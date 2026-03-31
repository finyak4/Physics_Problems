# 10. Animation: Wave Sources

## Problem Statement
Write an HTML animation in which it is possible to place dots that will serve as sources of waves described by the equation:
$$ u(\vec{r},t) = \frac{A}{|\vec{r}-\vec{r_0}|^\alpha} \sin(k |\vec{r} - \vec{r_0}| - \omega t) $$
where $\vec{r_0}$ is the position of the dot, and $\alpha$ is a parameter that can be set within the range $[0, 2]$. The animation should show the superposition of waves from all dots.

## Interactive Solution

Click anywhere inside the black canvas to place a wave source. Adjust the decay parameter ($\alpha$) to see how it affects the wave amplitude over distance.

<div id="wave-sources" style="margin-bottom: 2rem;">
  <div style="margin-bottom: 10px;">
    <label>Decay parameter $\alpha$: <strong id="alpha-val">0.5</strong></label><br>
    <input type="range" id="alpha-slider" min="0" max="2" step="0.1" value="0.5" style="width: 200px;">
    <button id="clear-btn" style="padding: 4px 10px; margin-left:15px; cursor: pointer; color: black; background: white; border: 1px solid #ccc; border-radius: 4px;">Clear Sources</button>
  </div>
  <canvas id="waves-canvas" width="400" height="400" style="background: black; border: 1px solid #ccc; cursor: crosshair;"></canvas>
  <p><small>Performance tip: placing too many dots without WebGL might reduce framerates!</small></p>
</div>

<script>
(function(){
  const canvas = document.getElementById("waves-canvas");
  const ctx = canvas.getContext("2d");
  const alphaSlider = document.getElementById("alpha-slider");
  const alphaVal = document.getElementById("alpha-val");
  const clearBtn = document.getElementById("clear-btn");
  
  const sources = [];
  const W = canvas.width;
  const H = canvas.height;
  
  // Create an offscreen buffer array for fast writing
  const imageData = ctx.createImageData(W, H);
  
  let time = 0;
  const k = 0.5;
  const omega = 1.0;
  const A = 40;
  
  alphaSlider.addEventListener('input', () => { alphaVal.textContent = alphaSlider.value; });
  clearBtn.addEventListener('click', () => { sources.length = 0; });
  canvas.addEventListener('click', (e) => {
    const rect = canvas.getBoundingClientRect();
    const x = e.clientX - rect.left;
    const y = e.clientY - rect.top;
    sources.push({x, y});
  });
  
  function render() {
    const alpha = parseFloat(alphaSlider.value);
    const data = imageData.data;
    
    let pos = 0;
    for(let y=0; y<H; y+=2) { // 2x2 blocks for slightly better performance
      for(let x=0; x<W; x+=2) {
        let u = 0;
        
        // Compute superposition at (x,y)
        for(let s=0; s<sources.length; s++) {
          const dx = x - sources[s].x;
          const dy = y - sources[s].y;
          const dist = Math.sqrt(dx*dx + dy*dy);
          if (dist < 0.1) continue;
          
          const amp = A / (Math.pow(dist, alpha) || 1);
          u += amp * Math.sin(k * dist - omega * time);
        }
        
        // Map abstract displacement to valid grayscale value (0 - 255)
        let col = 128 + u * 2;
        if(col > 255) col = 255; else if(col < 0) col = 0;
        
        // Write the same calculated pixel for a 2x2 chunk (optimization)
        for(let dy=0; dy<2; dy++) {
            for(let dx=0; dx<2; dx++) {
                const pxPos = ((y + dy) * W + (x + dx)) * 4;
                data[pxPos] = col;     // R
                data[pxPos+1] = col;   // G
                data[pxPos+2] = col;   // B
                data[pxPos+3] = 255;   // Alpha
            }
        }
      }
    }
    
    // Draw directly from buffer
    ctx.putImageData(imageData, 0, 0);
    
    // Overlay red UI dots on top of sources
    ctx.fillStyle = "red";
    for(let s=0; s<sources.length; s++) {
      ctx.beginPath();
      ctx.arc(sources[s].x, sources[s].y, 3, 0, 2*Math.PI);
      ctx.fill();
    }
    
    time += 0.25;
    requestAnimationFrame(render);
  }
  render();
})();
</script>

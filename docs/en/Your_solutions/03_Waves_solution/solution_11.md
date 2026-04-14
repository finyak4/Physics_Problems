# 11. Animation: Two-Slit Interference

## Problem Statement
Write an HTML animation simulating Young's experiment, in which two slits act as point sources of coherent waves. The displacement of the resultant wave is the sum of partial waves described by the formula:

$$ u(\vec{r},t) = \frac{A}{|\vec{r}-\vec{r_1}|} \sin(k |\vec{r} - \vec{r_1}| - \omega t) + \frac{A}{|\vec{r}-\vec{r_2}|} \sin(k |\vec{r} - \vec{r_2}| - \omega t) $$

where $\vec{r_1}$ and $\vec{r_2}$ are the position vectors of the slits. The user should be able to change the distance between the slits $d = |\vec{r_1} - \vec{r_2}|$ and the wavelength $\lambda$. The animation should visualize the resulting interference pattern in real time.

Open [animation](animations/03_11_anim.html).

## Interactive Solution

Adjust the slit distance $d$ and the wavelength $\lambda$. The corresponding interference pattern develops on the right. Dark banded regions define points of entirely destructive interference (standing nodes), whereas bright oscillating regions represent positive constructive interference (antinodes).

<div id="young-experiment" style="margin-bottom: 2rem;">
  <div style="display: flex; gap: 40px; align-items: center; margin-bottom: 15px;">
    <div>
      <label>Slit Distance ($d$): <strong id="d-val">40</strong> units</label><br>
      <input type="range" id="d-slider" min="10" max="100" step="5" value="40">
    </div>
    <div>
      <label>Wavelength ($\lambda$): <strong id="l-val">15</strong> units</label><br>
      <input type="range" id="l-slider" min="5" max="40" step="1" value="15">
    </div>
  </div>
  <canvas id="interference-canvas" width="500" height="400" style="background: black; border: 1px solid #ccc;"></canvas>
</div>

<script>
(function(){
  const canvas = document.getElementById("interference-canvas");
  const ctx = canvas.getContext("2d");
  const dSlider = document.getElementById("d-slider");
  const lSlider = document.getElementById("l-slider");
  const dVal = document.getElementById("d-val");
  const lVal = document.getElementById("l-val");
  
  const W = canvas.width;
  const H = canvas.height;
  const imageData = ctx.createImageData(W, H);
  
  let time = 0;
  const A = 150;
  const omega = 1.0;
  
  function updateLabels() {
    dVal.textContent = dSlider.value;
    lVal.textContent = lSlider.value;
  }
  dSlider.addEventListener('input', updateLabels);
  lSlider.addEventListener('input', updateLabels);
  
  function render() {
    const data = imageData.data;
    const d = parseFloat(dSlider.value);
    const lambda = parseFloat(lSlider.value);
    const k = 2 * Math.PI / lambda;
    
    // Position of slits (offset slightly on the X-axis)
    const x_slits = 40;
    const y_slit1 = H/2 - d/2;
    const y_slit2 = H/2 + d/2;
    
    for(let y=0; y<H; y+=2) { // Evaluate 2x2 blocks
      for(let x=0; x<W; x+=2) {
        let u = 0;
        
        // Only render the waves to the right side of the simulated barrier
        if (x > x_slits) {
            // Radial distance from slit 1
            const dx1 = x - x_slits;
            const dy1 = y - y_slit1;
            const dist1 = Math.sqrt(dx1*dx1 + dy1*dy1) || 0.1;

            // Radial distance from slit 2
            const dx2 = x - x_slits;
            const dy2 = y - y_slit2;
            const dist2 = Math.sqrt(dx2*dx2 + dy2*dy2) || 0.1;
            
            // Equation implementation, tweaked to 1/sqrt(r) to better preserve visual energy across the canvas
            let u1 = (A / Math.sqrt(dist1)) * Math.sin(k * dist1 - omega * time); 
            let u2 = (A / Math.sqrt(dist2)) * Math.sin(k * dist2 - omega * time);
            u = u1 + u2;
        }
        
        // Map superposition intensity to grayscale bounds (0 to 255)
        let col = 128 + u * 3;
        if (col < 0) col = 0; else if (col > 255) col = 255;
        
        // Write block pixel values
        for(let dy=0; dy<2; dy++) {
            for(let dx=0; dx<2; dx++) {
                const pos = ((y + dy) * W + (x + dx)) * 4;
                data[pos] = col;     // R
                data[pos+1] = col;   // G
                data[pos+2] = col;   // B
                data[pos+3] = 255;   // Alpha
            }
        }
      }
    }
    
    ctx.putImageData(imageData, 0, 0);
    
    // Draw the slit barrier visual component
    ctx.fillStyle = "#555";
    ctx.fillRect(x_slits - 5, 0, 10, y_slit1 - 2);
    ctx.fillRect(x_slits - 5, y_slit1 + 3, 10, d - 6);
    ctx.fillRect(x_slits - 5, y_slit2 + 3, 10, H - (y_slit2 + 3));
    
    time += 0.4;
    requestAnimationFrame(render);
  }
  
  render();
})();
</script>

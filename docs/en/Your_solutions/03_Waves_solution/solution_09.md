# 9. Damped Harmonic Oscillator

## Problem Statement
For the given equation describing a damped harmonic oscillator:
$$ m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + k x = 0 $$
make interactive HTML animation with a slider for the parameter $b$ to show the behavior of the system in the underdamped, critically damped, and overdamped cases.

1. Write down the general solution.
2. Present the classification of cases: underdamped, critically damped, overdamped.
3. Solve the equation numerically (RK4).
4. Investigate the effect of parameter $b$.
5. Generate the graph of $x(t)$.
6. Generate the phase portrait.

## Step-by-Step Theoretical Solution

The differential equation is:
$$ \frac{d^2 x}{dt^2} + \frac{b}{m} \frac{dx}{dt} + \frac{k}{m} x = 0 $$

We define the damping ratio $\gamma = \frac{b}{2m}$ and the natural angular frequency $\omega_0 = \sqrt{\frac{k}{m}}$. The equation is simplified:
$$ \ddot{x} + 2\gamma \dot{x} + \omega_0^2 x = 0 $$

### 1 & 2. General Solutions and Classification
The roots of the characteristic equation $r^2 + 2\gamma r + \omega_0^2 = 0$ dictate the nature of the solution, where $r = -\gamma \pm \sqrt{\gamma^2 - \omega_0^2}$.

*   **Underdamped case** ($\gamma < \omega_0$ or $b^2 < 4mk$):
    The roots are complex. The system oscillates with an exponentially decaying amplitude.
    $$ x(t) = A e^{-\gamma t} \cos(\omega_d t + \phi) $$
    where $\omega_d = \sqrt{\omega_0^2 - \gamma^2}$.

*   **Critically damped case** ($\gamma = \omega_0$ or $b^2 = 4mk$):
    The roots are real and identical. The system returns to equilibrium as fast as possible without oscillating.
    $$ x(t) = (A + Bt) e^{-\gamma t} $$

*   **Overdamped case** ($\gamma > \omega_0$ or $b^2 > 4mk$):
    The roots are real and distinct. The system experiences high drag and returns to equilibrium slowly without oscillating.
    $$ x(t) = A e^{r_1 t} + B e^{r_2 t} $$

### 3-6. Interactive Simulation (RK4, graph $x(t)$ and phase portrait)
Below is an interactive block solving the differential equation numerically in real-time using the 4th-order Runge-Kutta. Adjust the damping parameter $b$ using the slider to observe phase portraits and trajectories.

<div id="oscillator-sim" style="border:1px solid #ccc; padding: 15px; border-radius: 8px; background: #fafafa; color: #333;">
  <div>
    <label>Damping $b$: <strong id="b-val">0.5</strong> (underdamped)</label><br>
    <input type="range" id="b-slider" min="0" max="6" step="0.1" value="0.5" style="width: 100%;">
  </div>
  <div style="display: flex; gap: 10px; margin-top: 10px; flex-wrap: wrap;">
    <div style="text-align: center;">
      <canvas id="time-canvas" width="400" height="300" style="background: white; border: 1px solid #ddd;"></canvas>
      <br><small>Displacement $x(t)$ vs. Time $t$</small>
    </div>
    <div style="text-align: center;">
      <canvas id="phase-canvas" width="300" height="300" style="background: white; border: 1px solid #ddd;"></canvas>
      <br><small>Phase Portrait: Velocity $\dot{x}$ vs. position $x$</small>
    </div>
  </div>
</div>

<script>
(function(){
  const bSlider = document.getElementById("b-slider");
  const bVal = document.getElementById("b-val");
  const canvasT = document.getElementById("time-canvas");
  const ctxT = canvasT.getContext("2d");
  const canvasP = document.getElementById("phase-canvas");
  const ctxP = canvasP.getContext("2d");

  const m = 1.0;
  const k = 4.0;
  const criticalB = Math.sqrt(4 * m * k); // 4.0
  
  function draw() {
    const b = parseFloat(bSlider.value);
    
    let type = "underdamped";
    if (Math.abs(b - criticalB) < 0.1) type = "critically damped";
    else if (b > criticalB) type = "overdamped";
    else if (b === 0) type = "undamped";
    
    bVal.textContent = b.toFixed(1) + " (" + type + ")";
    
    // Initial conditions
    let x = 1.0;
    let v = 0.0;
    let t = 0.0;
    const dt = 0.05;
    const maxT = 20;
    
    const history = [{t, x, v}];
    
    // RK4
    const f = (x, v) => -(b/m)*v - (k/m)*x;
    
    while(t < maxT) {
      let k1x = v;
      let k1v = f(x, v);
      
      let k2x = v + k1v * dt / 2;
      let k2v = f(x + k1x * dt / 2, v + k1v * dt / 2);
      
      let k3x = v + k2v * dt / 2;
      let k3v = f(x + k2x * dt / 2, v + k2v * dt / 2);
      
      let k4x = v + k3v * dt;
      let k4v = f(x + k3x * dt, v + k3v * dt);
      
      x = x + (dt/6) * (k1x + 2*k2x + 2*k3x + k4x);
      v = v + (dt/6) * (k1v + 2*k2v + 2*k3v + k4v);
      t += dt;
      
      history.push({t, x, v});
    }
    
    // render time graph
    ctxT.clearRect(0, 0, canvasT.width, canvasT.height);
    ctxT.beginPath(); ctxT.moveTo(0, canvasT.height/2); ctxT.lineTo(canvasT.width, canvasT.height/2); ctxT.strokeStyle="#ccc"; ctxT.stroke();
    
    ctxT.beginPath();
    ctxT.strokeStyle = "blue";
    ctxT.lineWidth = 2;
    for(let i=0; i<history.length; i++) {
      let px = (history[i].t / maxT) * canvasT.width;
      let py = canvasT.height/2 - (history[i].x / 1.5) * (canvasT.height/2);
      if(i===0) ctxT.moveTo(px,py); else ctxT.lineTo(px,py);
    }
    ctxT.stroke();
    
    // render phase portrait
    ctxP.clearRect(0, 0, canvasP.width, canvasP.height);
    ctxP.beginPath(); ctxP.moveTo(0, canvasP.height/2); ctxP.lineTo(canvasP.width, canvasP.height/2); ctxP.strokeStyle="#ccc"; ctxP.stroke();
    ctxP.beginPath(); ctxP.moveTo(canvasP.width/2, 0); ctxP.lineTo(canvasP.width/2, canvasP.height); ctxP.strokeStyle="#ccc"; ctxP.stroke();
    
    ctxP.beginPath();
    ctxP.strokeStyle = "red";
    ctxP.lineWidth = 2;
    for(let i=0; i<history.length; i++) {
        // v on y-axis, x on x-axis
      let px = canvasP.width/2 + (history[i].x / 1.5) * (canvasP.width/2);
      let py = canvasP.height/2 - (history[i].v / 3.0) * (canvasP.height/2);
      if(i===0) ctxP.moveTo(px,py); else ctxP.lineTo(px,py);
    }
    ctxP.stroke();
  }
  
  bSlider.addEventListener("input", draw);
  draw();
})();
</script>

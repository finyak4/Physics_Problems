## 1. Projectile Motion

A projectile is fired from the ground with an initial velocity of $100 \text{ m/s}$ at an angle of $37^\circ$ above the horizontal. Assume no air resistance. Use $g = 9.81 \text{ m/s}^2$ and $\sin(37^\circ) \approx 0.6018, \cos(37^\circ) \approx 0.7986$.

**Step-by-step solution:**
1. **Differential equations of motion:**
   By Newton's second law, the only force is gravity $\vec{F} = (0, -mg)$.
   $m \frac{d^2x}{dt^2} = 0 \implies a_x = \frac{d^2x}{dt^2} = 0$
   $m \frac{d^2y}{dt^2} = -mg \implies a_y = \frac{d^2y}{dt^2} = -g$
2. **Time of flight ($T$):**
   The time of flight is the time it takes for the projectile to return to the ground ($y = 0$).
   $y(t) = v_{0y}t - \frac{1}{2}gt^2 = (v_0 \sin\theta)t - \frac{1}{2}gt^2 = 0$
   $t \left( v_0 \sin\theta - \frac{1}{2}gt \right) = 0$ 
   $t = 0$ (launch) or $T = \frac{2v_0 \sin\theta}{g}$
   $T = \frac{2(100)\sin(37^\circ)}{9.81} \approx \frac{200(0.6018)}{9.81} \approx 12.27 \text{ s}$
3. **Maximum height ($H$):**
   Occurs at $t = T/2$, when $v_y = 0$.
   $H = \frac{(v_0 \sin\theta)^2}{2g} = \frac{(100 \times 0.6018)^2}{2(9.81)} \approx \frac{3621.6}{19.62} \approx 184.59 \text{ m}$
4. **Range ($R$):**
   Horizontal distance at $t = T$.
   $R = v_{0x}T = \frac{v_0^2 \sin(2\theta)}{g} = \frac{(100)^2 \sin(74^\circ)}{9.81} \approx \frac{10000 \times 0.9613}{9.81} \approx 979.9 \text{ m}$

**Answer:**
- Diff. eqs: $\ddot{x} = 0, \ddot{y} = -g$
- Time of flight: $\approx 12.27 \text{ s}$
- Max height: $\approx 184.6 \text{ m}$
- Range: $\approx 979.9 \text{ m}$
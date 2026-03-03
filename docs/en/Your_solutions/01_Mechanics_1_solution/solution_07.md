## 7. Elimination of time and interpretation of acceleration

Path: $x(t)=2t^2, y(t)=3t^3$.

**Step-by-step solution:**
1. **Eliminate parameter $t$:**
   From $x = 2t^2$, assuming $t \ge 0$, we have $t = \sqrt{\frac{x}{2}}$.
   Substitute into $y$: $y = 3\left(\sqrt{\frac{x}{2}}\right)^3 = 3\left(\frac{x}{2}\right)^{3/2} = \frac{3}{2\sqrt{2}}x^{3/2}$.
2. **Trajectory curve:** It is a curve starting from the origin in the first quadrant, growing steeper as $x$ increases. Let's write it as $y^2 = \frac{9}{8}x^3$ (a semicubical parabola).
3. **Calculate vectors and magnitudes:**
   - Velocity: $\vec{v}(t) = (\frac{dx}{dt}, \frac{dy}{dt}) = (4t)\hat{i} + (9t^2)\hat{j}$
   - Speed (magnitude): $|\vec{v}(t)| = \sqrt{(4t)^2 + (9t^2)^2} = \sqrt{16t^2 + 81t^4} = t\sqrt{16 + 81t^2}$
   - Acceleration: $\vec{a}(t) = (\frac{d^2x}{dt^2}, \frac{d^2y}{dt^2}) = (4)\hat{i} + (18t)\hat{j}$
   - Magnitude of $\vec{a}$: $|\vec{a}(t)| = \sqrt{4^2 + (18t)^2} = \sqrt{16 + 324t^2}$
4. **Is acceleration constant?**
   No, since $\vec{a}(t)$ depends on time $t$ (specifically the $y$-component changes), the acceleration is continuously changing in magnitude and direction.

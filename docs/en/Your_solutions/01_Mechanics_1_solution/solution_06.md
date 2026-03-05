## 6. Variable Velocity

Velocity $v(t) = t^2 + 2t - 5$. At $t=0$, $x=4$. Find position and acceleration at $t=3$.

**Step-by-step solution:**
1. **Position calculation:** Integrate the velocity function.


   $x(t) = \int v(t) dt = \int (t^2 + 2t - 5) dt = \frac{t^3}{3} + t^2 - 5t + C$

2. Apply the initial condition $x(0) = 4$ to find $C$:

   $x(0) = 0 + 0 - 0 + C = 4 \implies C = 4$
   
   $x(t) = \frac{t^3}{3} + t^2 - 5t + 4$

3. Find position at $t=3$:

   $x(3) = \frac{3^3}{3} + 3^2 - 5(3) + 4 = 9 + 9 - 15 + 4 = 7$

4. **Acceleration calculation:** Differentiate the velocity function.

   $a(t) = \frac{dv}{dt} = 2t + 2$

5. Find acceleration at $t=3$:

   $a(3) = 2(3) + 2 = 8 \text{ m/s}^2$

**Answer:** $x(3) = 7 \text{ m}$, $a(3) = 8 \text{ m/s}^2$.
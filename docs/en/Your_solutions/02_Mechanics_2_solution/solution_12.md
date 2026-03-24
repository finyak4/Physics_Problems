# 12. Work and energy with a constant force

## Problem Statement

A constant force acts on a body of mass $m = 2\ \mathrm{kg}$:
$$ \vec F = [6, 2]\ \mathrm{N} $$
The body starts with an initial velocity $\vec v(0) = (1, -1)\ \mathrm{\frac{m}{s}}$ from the point $\vec r(0)=(0,0)\ \mathrm{m}$. 

* Determine $\vec a(t)$.
* Determine $\vec v(t)$.
* Determine $\vec r(t)$.
* Draw the trajectory of the motion.
* Calculate the work done by the force at time $t=3\ \mathrm{s}$.
* Check the consistency with the work-energy theorem.

## Step-by-Step Solution

**1. Determine $\vec a(t)$:**

- Since force is constant, acceleration is constant: $\vec{a}(t) = \frac{\vec{F}}{m}$.
  $$ \vec{a}(t) = \left[ \frac{6}{2}, \frac{2}{2} \right] = [3, 1] \, \text{m/s}^2 $$

**2. Determine $\vec v(t)$:**

- Velocity is the integral of acceleration: $\vec{v}(t) = \vec{a}t + \vec{v}_0$.
  $$ \vec{v}(t) = [3t, t] + [1, -1] = [3t + 1, \, t - 1] \, \text{m/s} $$

**3. Determine $\vec r(t)$:**

- Position is the integral of velocity: $\vec{r}(t) = \int \vec{v}(t) \, dt + \vec{r}_0$.
  $$ \vec{r}(t) = \left[ \frac{3}{2}t^2 + t, \, \frac{1}{2}t^2 - t \right] + [0, 0] = \left[ 1.5t^2 + t, \, 0.5t^2 - t \right] \, \text{m} $$

**4. Draw the trajectory of the motion:**

- The trajectory represents the path in the $xy$-plane. We can plot $y$ versus $x$ for times $t \geq 0$. This function is a parabola describing the constant acceleration path typical of projectile-like motion without gravity. To draw it mathematically or computationally, one would solve $x(t)$ for $t$ and plug it into $y(t)$, yielding a quadratic trajectory $y(x)$.

**5. Calculate the work done at time $t=3\ \mathrm{s}$:**

- The work done $W$ by a constant force is the dot product of force and displacement: $W = \vec{F} \cdot \Delta\vec{r}$.
- Evaluate $\vec{r}$ at $t=3$:
  $$ \vec{r}(3) = [1.5(3)^2 + 3, \, 0.5(3)^2 - 3] = [1.5(9) + 3, \, 0.5(9) - 3] = [13.5 + 3, \, 4.5 - 3] = [16.5, 1.5] \, \text{m} $$
- Calculate work:
  $$ W = \vec{F} \cdot \vec{r}(3) = (6)(16.5) + (2)(1.5) = 99 + 3 = 102 \, \text{J} $$

**6. Check consistency with the work-energy theorem:**

- Work-energy theorem states $W = \Delta K = K_f - K_i$.
- Calculate initial kinetic energy:
  $$ K_i = \frac{1}{2} m |\vec{v}_0|^2 = \frac{1}{2} (2) \left( 1^2 + (-1)^2 \right) = 1 \times 2 = 2 \, \text{J} $$
- Calculate final velocity at $t=3$:
  $$ \vec{v}(3) = [3(3) + 1, \, 3 - 1] = [10, 2] \, \text{m/s} $$
- Calculate final kinetic energy:
  $$ K_f = \frac{1}{2} m |\vec{v}(3)|^2 = \frac{1}{2} (2) \left( 10^2 + 2^2 \right) = 100 + 4 = 104 \, \text{J} $$
- Calculate the change in kinetic energy:
  $$ \Delta K = 104 - 2 = 102 \, \text{J} $$
- The work done ($102 \, \text{J}$) perfectly matches the change in kinetic energy ($102 \, \text{J}$), verifying the theorem.

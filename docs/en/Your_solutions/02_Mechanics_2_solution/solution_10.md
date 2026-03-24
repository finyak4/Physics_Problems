# 10. Force field and power

## Problem Statement
In a certain force field, the equations of motion of a particle with mass $m=0.5$ kg are as follows:
$$ x = 5t^2 - t, \quad y = 2t^3, \quad z = -3t + 2 $$
Find the time dependence of: the particle's velocity, the particle's momentum, the particle's acceleration, the force acting on the particle, and the power transferred by the field to the particle.

## Step-by-Step Solution

**1. Velocity $\vec{v}(t)$:**
- Velocity is the first derivative of the position vector $\vec{r}(t) = [x, y, z]$ with respect to time.
  $$ \vec{v}(t) = \left[ \frac{dx}{dt}, \frac{dy}{dt}, \frac{dz}{dt} \right] $$
  $$ v_x = \frac{d}{dt}(5t^2 - t) = 10t - 1 $$
  $$ v_y = \frac{d}{dt}(2t^3) = 6t^2 $$
  $$ v_z = \frac{d}{dt}(-3t + 2) = -3 $$
- Therefore: $\vec{v}(t) = [10t - 1, \, 6t^2, \, -3] \, \text{m/s}$

**2. Momentum $\vec{p}(t)$:**
- Momentum is mass times velocity: $\vec{p}(t) = m\vec{v}(t)$.
- Given $m = 0.5 \text{ kg}$:
  $$ \vec{p}(t) = 0.5 \times [10t - 1, \, 6t^2, \, -3] = [5t - 0.5, \, 3t^2, \, -1.5] \, \text{kg m/s} $$

**3. Acceleration $\vec{a}(t)$:**
- Acceleration is the first derivative of velocity with respect to time.
  $$ \vec{a}(t) = \left[ \frac{dv_x}{dt}, \frac{dv_y}{dt}, \frac{dv_z}{dt} \right] $$
  $$ a_x = \frac{d}{dt}(10t - 1) = 10 $$
  $$ a_y = \frac{d}{dt}(6t^2) = 12t $$
  $$ a_z = \frac{d}{dt}(-3) = 0 $$
- Therefore: $\vec{a}(t) = [10, \, 12t, \, 0] \, \text{m/s}^2$

**4. Force $\vec{F}(t)$:**
- Using Newton's Second Law, $\vec{F}(t) = m\vec{a}(t)$.
  $$ \vec{F}(t) = 0.5 \times [10, \, 12t, \, 0] = [5, \, 6t, \, 0] \, \text{N} $$

**5. Power $P(t)$:**
- Power is the dot product of force and velocity: $P(t) = \vec{F}(t) \cdot \vec{v}(t)$.
  $$ P(t) = F_x v_x + F_y v_y + F_z v_z $$
  $$ P(t) = (5)(10t - 1) + (6t)(6t^2) + (0)(-3) $$
  $$ P(t) = 50t - 5 + 36t^3 $$
- Therefore, the power transferred is $P(t) = 36t^3 + 50t - 5 \, \text{W}$.

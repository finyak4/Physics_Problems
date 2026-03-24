# 11. Dynamics with a time-dependent force

## Problem Statement
A particle of mass $m=3$ kg moves in a force field $F$ dependent on time in the following way:
$$ F = (15t, 3t-12, -6t^2) \, \text{N} $$
Assuming initial conditions $r_0=(5,2,-3)$ m, $v_0=(2,0,1)$ m/s, find the dependence of the particle's position and velocity on time.

## Step-by-Step Solution

**1. Determine acceleration:**
- From Newton's Second Law, $\vec{a}(t) = \frac{\vec{F}(t)}{m}$.
- Given $m = 3 \text{ kg}$:
  $$ \vec{a}(t) = \left[ \frac{15t}{3}, \frac{3t-12}{3}, \frac{-6t^2}{3} \right] = [5t, \, t-4, \, -2t^2] \, \text{m/s}^2 $$

**2. Determine velocity $\vec{v}(t)$:**
- Velocity is the integral of acceleration: $\vec{v}(t) = \int \vec{a}(t) dt + \vec{v}_0$.
  $$ v_x(t) = \int 5t \, dt = \frac{5}{2}t^2 + C_x $$
  $$ v_y(t) = \int (t-4) \, dt = \frac{1}{2}t^2 - 4t + C_y $$
  $$ v_z(t) = \int (-2t^2) \, dt = -\frac{2}{3}t^3 + C_z $$
- Use the initial velocity $v_0 = (2, 0, 1)$ at $t=0$:
  $$ v_x(0) = 0 + C_x = 2 \implies C_x = 2 $$
  $$ v_y(0) = 0 + C_y = 0 \implies C_y = 0 $$
  $$ v_z(0) = 0 + C_z = 1 \implies C_z = 1 $$
- So, the velocity is:
  $$ \vec{v}(t) = \left[ \frac{5}{2}t^2 + 2, \, \frac{1}{2}t^2 - 4t, \, -\frac{2}{3}t^3 + 1 \right] \, \text{m/s} $$

**3. Determine position $\vec{r}(t)$:**
- Position is the integral of velocity: $\vec{r}(t) = \int \vec{v}(t) dt + \vec{r}_0$.
  $$ x(t) = \int \left( \frac{5}{2}t^2 + 2 \right) dt = \frac{5}{6}t^3 + 2t + K_x $$
  $$ y(t) = \int \left( \frac{1}{2}t^2 - 4t \right) dt = \frac{1}{6}t^3 - 2t^2 + K_y $$
  $$ z(t) = \int \left( -\frac{2}{3}t^3 + 1 \right) dt = -\frac{1}{6}t^4 + t + K_z $$
- Use the initial position $r_0 = (5, 2, -3)$ at $t=0$:
  $$ x(0) = 0 + K_x = 5 \implies K_x = 5 $$
  $$ y(0) = 0 + K_y = 2 \implies K_y = 2 $$
  $$ z(0) = 0 + K_z = -3 \implies K_z = -3 $$
- So, the position is:
  $$ \vec{r}(t) = \left[ \frac{5}{6}t^3 + 2t + 5, \, \frac{1}{6}t^3 - 2t^2 + 2, \, -\frac{1}{6}t^4 + t - 3 \right] \, \text{m} $$

# 9. Vertical throw with drag

## Problem Statement

We have the equation of motion:
$$ m\frac{dv}{dt} = -mg - kv $$
with initial conditions $v(0)=v_0$, $x(0)=10$.

* Solve the equation by analytical methods.
* Determine the maximum height.
* Compare with the case without drag.
* Perform a numerical simulation using HTML or Python.

## Step-by-Step Solution

**1. Solve the equation analytically:**

- The equation of motion is:
  $$ m \frac{dv}{dt} = -mg - kv \implies \frac{dv}{dt} = -g - \frac{k}{m}v $$
- Rearrange to separate variables:
  $$ \frac{dv}{g + \frac{k}{m}v} = -dt $$
- Integrate both sides, from $t=0$ to $t$, and $v(0)=v_0$ to $v(t)$:
  $$ \int_{v_0}^v \frac{dv}{g + \frac{k}{m}v} = \int_0^t -dt $$
  $$ \frac{m}{k} \ln \left| \frac{g + \frac{k}{m}v}{g + \frac{k}{m}v_0} \right| = -t $$
- Solve for $v(t)$:
  $$ g + \frac{k}{m}v = \left( g + \frac{k}{m}v_0 \right) e^{-\frac{kt}{m}} $$
  $$ v(t) = \left( \frac{mg}{k} + v_0 \right) e^{-\frac{kt}{m}} - \frac{mg}{k} $$
- To find $x(t)$, integrate $v(t)$ with respect to time using $x(0) = 10$:
  $$ x(t) = 10 + \int_0^t v(\tau) \, d\tau $$
  $$ x(t) = 10 + \left( \frac{mg}{k} + v_0 \right) \left[ -\frac{m}{k} e^{-\frac{k\tau}{m}} \right]_0^t - \frac{mg}{k}t $$
  $$ x(t) = 10 + \frac{m}{k} \left( v_0 + \frac{mg}{k} \right) \left( 1 - e^{-\frac{kt}{m}} \right) - \frac{mg}{k}t $$

**2. Determine the maximum height:**

- Maximum height is reached when velocity becomes $0$ ($v(t_{\text{top}}) = 0$).
- Using the velocity formula:
  $$ 0 = \left( \frac{mg}{k} + v_0 \right) e^{-\frac{kt_{\text{top}}}{m}} - \frac{mg}{k} $$
  $$ e^{\frac{kt_{\text{top}}}{m}} = \frac{v_0 k}{mg} + 1 \implies t_{\text{top}} = \frac{m}{k} \ln\left( 1 + \frac{kv_0}{mg} \right) $$
- Substitute $t_{\text{top}}$ into $x(t)$ to find $H_{\text{max}}$. After simplifying:
  $$ H_{\text{max}} = 10 + \frac{m v_0}{k} - \frac{m^2 g}{k^2} \ln\left( 1 + \frac{k v_0}{m g} \right) $$

**3. Compare with the case without drag:**

- Without drag ($k=0$), $t_{\text{top}} = \frac{v_0}{g}$ and $H_{\text{max}} = 10 + \frac{v_0^2}{2g}$.
- The presence of the drag force means that the maximum height achieved with drag will be strictly less than without drag, because kinetic energy is continuously dissipated by the drag force.


[Open the demo](animations/02_09_anim.html)

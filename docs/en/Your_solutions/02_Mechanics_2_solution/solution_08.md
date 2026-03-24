# 8. Work of a variable force

## Problem Statement

Given a one-dimensional force:
$$ F(x)=-kx $$

* Write down the equation of motion and solve it.
* Calculate the work done during the displacement from $0$ to $x_0$.
* Interpret the result as potential energy.
* Verify the relationship $F = -\frac{dU}{dx}$.
* Draw the graph of $F(x)$ and $U(x)$.

## Step-by-Step Solution

**1. Equation of motion and its solution:**

- According to Newton's Second Law, $F = ma = m\frac{d^2x}{dt^2}$.
- Therefore, the equation of motion is:
  $$ m\frac{d^2x}{dt^2} = -kx \implies \frac{d^2x}{dt^2} + \frac{k}{m}x = 0 $$
- Let $\omega^2 = \frac{k}{m}$. The equation becomes a standard harmonic oscillator equation:
  $$ \frac{d^2x}{dt^2} + \omega^2 x = 0 $$
- The general solution is:
  $$ x(t) = A \cos(\omega t + \phi) $$

**2. Work done during displacement from $0$ to $x_0$:**

- The work $W$ done by the force is given by the integral of $F(x)$:
  $$ W = \int_0^{x_0} F(x) \, dx = \int_0^{x_0} -kx \, dx $$
- Evaluating the integral:
  $$ W = -k \left[ \frac{x^2}{2} \right]_0^{x_0} = -\frac{1}{2} k x_0^2 $$

**3. Interpret the result as potential energy:**

- The work done by a conservative force equals the negative change in potential energy ($\Delta U = -W$).
- Assuming $U(0) = 0$, we have:
  $$ U(x_0) - U(0) = -W \implies U(x_0) = -\left(-\frac{1}{2} k x_0^2\right) = \frac{1}{2} k x_0^2 $$
- The potential energy stored in the system (e.g., a spring) at position $x$ is $U(x) = \frac{1}{2} k x^2$.

**4. Verify the relationship $F = -\frac{dU}{dx}$:**

- We have the potential energy function $U(x) = \frac{1}{2} k x^2$.
- Take the negative derivative with respect to $x$:
  $$ -\frac{dU}{dx} = -\frac{d}{dx} \left( \frac{1}{2} k x^2 \right) = -\frac{1}{2} k (2x) = -kx $$
- This matches the original force $F(x) = -kx$, verifying the relationship.

**5. Graphs of $F(x)$ and $U(x)$:**

- **$F(x) = -kx$:** This is a straight line passing through the origin with a negative slope $-k$.
- **$U(x) = \frac{1}{2}kx^2$:** This is an upward-opening parabola with its vertex at the origin completely above or on the x-axis.

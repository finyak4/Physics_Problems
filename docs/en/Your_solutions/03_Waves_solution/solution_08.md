# 8. Waves Function Check

## Problem Statement
Which of the following functions can describe a traveling wave? Hint: check if it satisfies the wave equation:
$$ \frac{\partial^2 y}{\partial x^2} = \frac{1}{v^2} \frac{\partial^2 y}{\partial t^2} $$
a) $y(x,t) = A \cos(kx^2 - \omega t)$
b) $y(x,t) = A(x-vt)^2$
c) $y(x,t) = A \log(x+vt)$

## Step-by-Step Solution

To be a valid general wave function, $y(x,t)$ must satisfy the 1D linear wave equation. Alternatively, any function of the form $f(x \pm vt)$ is a valid solution.

---

### a) $y(x,t) = A \cos(kx^2 - \omega t)$

1. **Find the second partial derivative with respect to $x$:**
   $$ \frac{\partial y}{\partial x} = -A \sin(kx^2 - \omega t) \cdot (2kx) $$
   By the product rule:
   $$ \frac{\partial^2 y}{\partial x^2} = -2Ak \left[ \sin(kx^2 - \omega t) + x \cos(kx^2 - \omega t) \cdot (2kx) \right] $$
   $$ \frac{\partial^2 y}{\partial x^2} = -2Ak \sin(kx^2 - \omega t) - 4Ak^2x^2 \cos(kx^2 - \omega t) $$

2. **Find the second partial derivative with respect to $t$:**
   $$ \frac{\partial y}{\partial t} = -A \sin(kx^2 - \omega t) \cdot (-\omega) = A\omega \sin(kx^2 - \omega t) $$
   $$ \frac{\partial^2 y}{\partial t^2} = -A\omega^2 \cos(kx^2 - \omega t) $$

3. Comparing the two second derivatives, no constant scale factor $\frac{1}{v^2}$ can equate them due to the extra sine and $x^2$ elements in the spatial derivative.
   **Conclusion: No, it is not a traveling wave.**

---

### b) $y(x,t) = A(x-vt)^2$

1. **Find the second partial derivative with respect to $x$:**
   $$ \frac{\partial y}{\partial x} = 2A(x - vt) $$
   $$ \frac{\partial^2 y}{\partial x^2} = 2A $$

2. **Find the second partial derivative with respect to $t$:**
   $$ \frac{\partial y}{\partial t} = 2A(x - vt) \cdot (-v) = -2Av(x - vt) $$
   $$ \frac{\partial^2 y}{\partial t^2} = -2Av(-v) = 2Av^2 $$

3. Substitute into the wave equation $\frac{\partial^2 y}{\partial x^2} = \frac{1}{v^2} \frac{\partial^2 y}{\partial t^2}$:
   $$ 2A = \frac{1}{v^2} (2Av^2) $$
   $$ 2A = 2A $$
   Both sides are perfectly equal.
   **Conclusion: Yes, it describes a traveling wave.**

---

### c) $y(x,t) = A \log(x+vt)$

1. **Find the second partial derivative with respect to $x$:**
   $$ \frac{\partial y}{\partial x} = \frac{A}{x+vt} $$
   $$ \frac{\partial^2 y}{\partial x^2} = -\frac{A}{(x+vt)^2} $$

2. **Find the second partial derivative with respect to $t$:**
   $$ \frac{\partial y}{\partial t} = A \frac{v}{x+vt} $$
   $$ \frac{\partial^2 y}{\partial t^2} = -A \frac{v^2}{(x+vt)^2} $$

3. Substitute into the wave equation $\frac{\partial^2 y}{\partial x^2} = \frac{1}{v^2} \frac{\partial^2 y}{\partial t^2}$:
   $$ -\frac{A}{(x+vt)^2} = \frac{1}{v^2} \left( -A \frac{v^2}{(x+vt)^2} \right) $$
   $$ -\frac{A}{(x+vt)^2} = -\frac{A}{(x+vt)^2} $$
   Both sides are equal.
   **Conclusion: Yes, it describes a traveling wave.**

# 3. Superposition Principle

## Problem Statement
Two waves are described by the equations $y_1(x, t) = A \sin(kx - \omega t)$ and $y_2(x, t) = A \sin(kx + \omega t)$. What is the equation of the resulting standing wave? Identify the positions of the nodes.

## Step-by-Step Solution

**Part 1: Equation of the Standing Wave**

1. By the superposition principle, the resulting wave ($y$) is the sum of the two individual waves:
   $$ y(x,t) = y_1(x,t) + y_2(x,t) $$
   $$ y(x,t) = A \sin(kx - \omega t) + A \sin(kx + \omega t) $$

2. Use the trigonometric identity for the sum of sines:
   $$ \sin(\alpha) + \sin(\beta) = 2 \sin\left(\frac{\alpha + \beta}{2}\right) \cos\left(\frac{\alpha - \beta}{2}\right) $$
   Here, let $\alpha = kx + \omega t$ and $\beta = kx - \omega t$ (since $\sin$ is odd, $\sin(kx - \omega t) + \sin(kx + \omega t)$ is the same).

3. Set up $\alpha$ and $\beta$:
   - $\alpha = kx - \omega t$
   - $\beta = kx + \omega t$

   $$ y(x,t) = A \left[ 2 \sin\left(\frac{(kx - \omega t) + (kx + \omega t)}{2}\right) \cos\left(\frac{(kx - \omega t) - (kx + \omega t)}{2}\right) \right] $$

4. Simplify the terms:
   $$ \frac{\alpha + \beta}{2} = \frac{2kx}{2} = kx $$
   $$ \frac{\alpha - \beta}{2} = \frac{-2\omega t}{2} = -\omega t $$

   This gives:
   $$ y(x,t) = 2A \sin(kx) \cos(-\omega t) $$

5. Since cosine is an even function ($\cos(-\theta) = \cos(\theta)$):
   $$ y(x,t) = 2A \sin(kx) \cos(\omega t) $$
   This is the standard equation of a standing wave.

---

**Part 2: Position of the Nodes**

1. Nodes are points that are always at rest. At roughly any time $t$, their displacement is exactly zero ($y = 0$).
2. Based on the equation $y(x,t) = [2A \sin(kx)] \cos(\omega t)$, the displacement is persistently zero when the amplitude term disappears:
   $$ \sin(kx) = 0 $$

3. The function $\sin(\theta)$ is zero whenever its argument is an integer multiple of $\pi$:
   $$ kx = n\pi \quad (\text{where } n = 0, \pm 1, \pm 2, \dots) $$

4. The wave number $k$ is defined in terms of the wavelength $\lambda$ as $k = \frac{2\pi}{\lambda}$. Substitute this for $k$:
   $$ \frac{2\pi}{\lambda} x = n\pi $$

5. Solve for $x$:
   $$ x = \frac{n\pi \lambda}{2\pi} = \frac{nd\lambda}{2} $$
   So the nodes occur at positions:
   $$ x = 0, \frac{\lambda}{2}, \lambda, \frac{3\lambda}{2}, \dots $$

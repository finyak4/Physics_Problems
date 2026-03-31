# 6. Wave Equation

## Problem Statement
A wave is described by the equation $y(x,t) = 0.05 \sin(2\pi x - 50\pi t)$, where $x$ and $y$ are in meters and $t$ is in seconds. Determine the waves':
a) Amplitude $A$.
b) Wavelength $\lambda$.
c) Frequency $f$.
d) Wave speed $v$.

## Step-by-Step Solution

1. The general equation of a sinusoidal traveling wave is defined as:
   $$ y(x,t) = A \sin(kx - \omega t) $$

2. By directly comparing the standard equation to the given equation $y(x,t) = 0.05 \sin(2\pi x - 50\pi t)$, we can identify the following matching parameters:
   - Amplitude: $A = 0.05\text{ m}$
   - Wave number: $k = 2\pi\text{ rad/m}$
   - Angular frequency: $\omega = 50\pi\text{ rad/s}$

---

**a) Amplitude $A$**

It can be extracted directly from the multiplied constant on the outside of the sine function:
$$ \mathbf{A = 0.05\text{ m}} $$

---

**b) Wavelength $\lambda$**

The wave number ($k$) intrinsically relates to the wavelength by the formula $k = \frac{2\pi}{\lambda}$.
1. Substitute $k = 2\pi$:
   $$ 2\pi = \frac{2\pi}{\lambda} $$
2. Rearranging gives:
   $$ \mathbf{\lambda = 1\text{ m}} $$

---

**c) Frequency $f$**

The angular frequency ($\omega$) is connected to the ordinary frequency $f$ by the formula $\omega = 2\pi f$.
1. Substitute $\omega = 50\pi$:
   $$ 50\pi = 2\pi f $$
2. Isolate $f$ by dividing by $2\pi$:
   $$ f = \frac{50\pi}{2\pi} $$
   $$ \mathbf{f = 25\text{ Hz}} $$

---

**d) Wave speed $v$**

The speed of the wave can be calculated directly using either $v = f \cdot \lambda$ or $v = \frac{\omega}{k}$.
1. Using the results from b and c ($f = 25\text{ Hz}$ and $\lambda = 1\text{ m}$):
   $$ v = 25\text{ Hz} \cdot 1\text{ m} $$
   $$ \mathbf{v = 25\text{ m/s}} $$

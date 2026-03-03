## 10. Infinite Series

Moves: 1 m east, 1/2 m north, 1/3 m west, 1/4 m south, 1/5 m east, and so on.

**Step-by-step solution:**

1. Separate the horizontal ($x$) and vertical ($y$) movements.

   - East and West represent the $x$-axis.
   - North and South represent the $y$-axis.

2. The horizontal series is constructed by alternating terms at odd positions:

   - $x = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \dots$
   This is the well-known Gregory-Leibniz series for the arctangent function evaluated at 1:
   $\sum_{n=0}^{\infty} \frac{(-1)^n}{2n+1} = \arctan(1) = \frac{\pi}{4}$

3. The vertical series is constructed by alternating terms at even positions:

   - $y = \frac{1}{2} - \frac{1}{4} + \frac{1}{6} - \frac{1}{8} + \dots$
   We can factor out $\frac{1}{2}$ to see the alternating harmonic series:
   $y = \frac{1}{2} \left(1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \dots \right)$
   Since the alternating harmonic series converges to $\ln(2)$, we get:
   $y = \frac{1}{2} \ln(2) = \ln(\sqrt{2})$

**Answer:** The final position is $\left(\frac{\pi}{4}, \frac{\ln(2)}{2}\right)$.
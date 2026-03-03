## 9. Optimization Problem

Rectangle under $y = 3 - x^2$ in the first quadrant. Maximum area dimensions?

**Step-by-step solution:**

1. Let the top right corner of the rectangle on the curve be $(x, y)$. Since it's in the first quadrant, $x > 0$ and $y > 0$.

2. The width of the rectangle is $x$ and the height is $y = 3 - x^2$.

3. The formula for the area is $A(x) = x \cdot y = x(3 - x^2) = 3x - x^3$.

4. Take the derivative of $A(x)$ with respect to $x$ and set it to zero:

   $A'(x) = 3 - 3x^2 = 0$
   $3x^2 = 3 \implies x^2 = 1 \implies x = 1$ (since $x > 0$)

5. Verify it's a maximum using the second derivative:

   $A''(x) = -6x \implies A''(1) = -6 < 0$ (confirming a maximum).

6. Find the corresponding height $y$:

   $y = 3 - (1)^2 = 2$

**Answer:** Width $x = 1$, Height $y = 2$. Maximum area is $2$.
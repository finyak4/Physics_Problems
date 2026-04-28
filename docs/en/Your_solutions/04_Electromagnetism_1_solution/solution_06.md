# 6. Field at a point from a system of charges

**Problem:**
Two point charges are given:
* $+q\  \text{at point}\  (-a, 0)$
* $+2q\  \text{at point}\  (a, 0)$

1. Determine the field vector $\vec E(0, y)$, $\vec E(x, 0)$ and generally $\vec E(x, y)$.
2. Determine the condition for which the components $E_x = 0$, $E_y = 0$ and the zero field $\vec E = 0$.
3. Calculate the field for: $a = 0.2\text{ m}$, $y = 0.3\text{ m}$, $q = 2\mu\text{C}$.
4. Investigate the limit $y \gg a$.

**Solution:**

Let the position vectors of the charges be $\vec{r}_1 = -a\hat{i} + 0\hat{j}$ and $\vec{r}_2 = a\hat{i} + 0\hat{j}$.
The electric field at a position $\vec{r} = x\hat{i} + y\hat{j}$ is:
$$ \vec{E}(\vec{r}) = \vec{E}_1(\vec{r}) + \vec{E}_2(\vec{r}) = \frac{k(q)}{|\vec{r} - \vec{r}_1|^3}(\vec{r} - \vec{r}_1) + \frac{k(2q)}{|\vec{r} - \vec{r}_2|^3}(\vec{r} - \vec{r}_2) $$

**1. Determine the field vectors**

**Generally $\vec{E}(x,y)$:**
$$ \vec{r} - \vec{r}_1 = (x+a)\hat{i} + y\hat{j} $$
$$ |\vec{r} - \vec{r}_1| = \sqrt{(x+a)^2 + y^2} $$
$$ \vec{r} - \vec{r}_2 = (x-a)\hat{i} + y\hat{j} $$
$$ |\vec{r} - \vec{r}_2| = \sqrt{(x-a)^2 + y^2} $$

$$ \vec{E}(x,y) = kq \left[ \frac{(x+a)\hat{i} + y\hat{j}}{((x+a)^2 + y^2)^{3/2}} + \frac{2((x-a)\hat{i} + y\hat{j})}{((x-a)^2 + y^2)^{3/2}} \right] $$

Thus:

$$ E_x(x,y) = kq \left[ \frac{x+a}{((x+a)^2 + y^2)^{3/2}} + \frac{2(x-a)}{((x-a)^2 + y^2)^{3/2}} \right] $$

$$ E_y(x,y) = kq y \left[ \frac{1}{((x+a)^2 + y^2)^{3/2}} + \frac{2}{((x-a)^2 + y^2)^{3/2}} \right] $$

**For $\vec{E}(0,y)$:**
Substitute $x = 0$:
$$ E_x(0,y) = kq \left[ \frac{a}{(a^2 + y^2)^{3/2}} - \frac{2a}{(a^2 + y^2)^{3/2}} \right] = -\frac{kq a}{(a^2 + y^2)^{3/2}} $$
$$ E_y(0,y) = kq y \left[ \frac{1}{(a^2 + y^2)^{3/2}} + \frac{2}{(a^2 + y^2)^{3/2}} \right] = \frac{3kq y}{(a^2 + y^2)^{3/2}} $$
$$ \vec{E}(0,y) = \frac{kq}{(a^2 + y^2)^{3/2}} (-a\hat{i} + 3y\hat{j}) $$

**For $\vec{E}(x,0)$:**
Substitute $y = 0$:
$$ E_y(x,0) = 0 $$
$$ E_x(x,0) = kq \left[ \frac{x+a}{|x+a|^3} + \frac{2(x-a)}{|x-a|^3} \right] = kq \left[ \frac{\text{sgn}(x+a)}{(x+a)^2} + \frac{2\text{sgn}(x-a)}{(x-a)^2} \right] $$
$$ \vec{E}(x,0) = kq \left[ \frac{\text{sgn}(x+a)}{(x+a)^2} + \frac{2\text{sgn}(x-a)}{(x-a)^2} \right] \hat{i} $$

**2. Condition for zero components**
* **$E_y = 0$ condition:**
$E_y(x,y) = 0$ requires $y \left[ \frac{1}{((x+a)^2 + y^2)^{3/2}} + \frac{2}{((x-a)^2 + y^2)^{3/2}} \right] = 0$. Since the bracket is strictly positive, the only condition is $y = 0$.
* **$E_x = 0$ condition:**
Requires $\frac{x+a}{((x+a)^2 + y^2)^{3/2}} + \frac{2(x-a)}{((x-a)^2 + y^2)^{3/2}} = 0$.
* **Zero field $\vec{E}=0$ condition:**
Must have both $E_y = 0$ and $E_x = 0$. Note that $E_y = 0$ implies $y = 0$. Thus the condition for zero field occurs on the x-axis ($y=0$):

$$ \frac{\text{sgn}(x+a)}{(x+a)^2} + \frac{2\text{sgn}(x-a)}{(x-a)^2} = 0 $$

For this to hold, the terms must have opposite signs. This means $\text{sgn}(x+a) = 1$ and $\text{sgn}(x-a) = -1$, meaning the point must lie strictly between the two charges: $-a < x < a$.
Then:

$$ \frac{1}{(x+a)^2} - \frac{2}{(x-a)^2} = 0 \Rightarrow (x-a)^2 = 2(x+a)^2 $$

Taking the square root (noting $x-a$ is negative and $x+a$ is positive):

$$ -(x-a) = \sqrt{2}(x+a) \Rightarrow a - x = \sqrt{2}x + a\sqrt{2} \Rightarrow x(1+\sqrt{2}) = a(1-\sqrt{2}) $$

$$ x = a \frac{1-\sqrt{2}}{1+\sqrt{2}} = a \frac{(1-\sqrt{2})^2}{1-2} = -a(3 - 2\sqrt{2}) \approx -0.17a $$



Therefore, $\vec{E}=0$ at the point $(-a(3-2\sqrt{2}), 0)$.

**3. Calculate field for $a=0.2\text{ m}$, $y=0.3\text{ m}$, $q=2\mu\text{C}$**
We evaluate at $(0, y) = (0, 0.3)$:
$$ a = 0.2, \quad y = 0.3, \quad q = 2\times 10^{-6}\text{ C}, \quad k \approx 8.99\times 10^9 $$
$a^2 + y^2 = 0.2^2 + 0.3^2 = 0.04 + 0.09 = 0.13$
$ (a^2+y^2)^{3/2} = 0.13^{3/2} \approx 0.04687 $
Using the $\vec{E}(0,y)$ formula:
$$ \vec{E}(0, 0.3) = \frac{(8.99\times 10^9)(2\times 10^{-6})}{0.04687} (-0.2\hat{i} + 3(0.3)\hat{j}) $$
$$ = \frac{17.98\times 10^3}{0.04687} (-0.2\hat{i} + 0.9\hat{j}) \approx 383614 (-0.2\hat{i} + 0.9\hat{j})\text{ V/m} $$
$$ \vec{E}(0, 0.3) \approx (-7.67\times 10^4 \hat{i} + 3.45\times 10^5 \hat{j})\text{ V/m} $$

**4. Investigate the limit $y \gg a$**
If we look at $\vec{E}(0,y)$ as $y \to \infty$:
$$ (a^2+y^2)^{3/2} = y^3 \left(1 + \frac{a^2}{y^2}\right)^{3/2} \approx y^3 $$
$$ \vec{E}(0,y) \approx \frac{kq}{y^3} (-a\hat{i} + 3y\hat{j}) = -\frac{kqa}{y^3}\hat{i} + \frac{3kq}{y^2}\hat{j} $$
Since $1/y^2$ dominates $1/y^3$ for large $y$, the field points predominantly in the $+\hat{j}$ direction and behaves as:
$$ \vec{E}(0,y) \approx \frac{k(3q)}{y^2} \hat{j} $$
This is consistent with the field of a single point charge of magnitude $Q_{net} = q + 2q = 3q$ placed at the origin, meaning from far away, the charge distribution looks roughly like a single combined point charge of $+3q$.

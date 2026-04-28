# 2. Electric Potential

**Problem:**
Point charges of $+1\text{C}$, $-2\text{C}$, $+3\text{C}$, and $-4\text{C}$ are placed at the corners of a square with sides of $1.0\text{ m}$ (in order). Calculate the electric potential at the center of the square.

**Solution:**
The electric potential $V$ at a point due to a system of point charges is the algebraic sum of the potentials due to each individual charge:
$$ V = \sum_{i} V_i = \sum_{i} k \frac{q_i}{r_i} $$
where $k$ is Coulomb's constant ($k \approx 8.99 \times 10^9\text{ N m}^2 / \text{C}^2$), $q_i$ are the individual charges, and $r_i$ is the distance from each charge to the point of interest.

Let the side of the square be $a = 1.0\text{ m}$. 
The distance from any corner of the square to its center is half the length of the diagonal:
$$ r_1 = r_2 = r_3 = r_4 = r = \frac{a\sqrt{2}}{2} = \frac{1.0\text{ m}}{\sqrt{2}} = \frac{\sqrt{2}}{2}\text{ m} $$

The given charges are:
* $q_1 = +1\text{ C}$
* $q_2 = -2\text{ C}$
* $q_3 = +3\text{ C}$
* $q_4 = -4\text{ C}$

Substitute these values into the potential formula:
$$ V = k \left( \frac{q_1}{r} + \frac{q_2}{r} + \frac{q_3}{r} + \frac{q_4}{r} \right) = \frac{k}{r} (q_1 + q_2 + q_3 + q_4) $$

Calculate the sum of the charges:
$$ \sum_{i=1}^4 q_i = +1 - 2 + 3 - 4 = -2\text{ C} $$

Now, plug in the values for $k$, $r$, and the sum of charges:
$$ V = \frac{8.99 \times 10^9}{\frac{\sqrt{2}}{2}} \cdot (-2) $$
$$ V = 8.99 \times 10^9 \cdot \sqrt{2} \cdot (-2) $$
$$ V = -17.98 \times 10^9 \cdot \sqrt{2} \approx -17.98 \times 10^9 \cdot 1.414 $$
$$ V \approx -2.54 \times 10^{10}\text{ V} $$

**Answer:**
The electric potential at the center of the square is approximately **$-2.54 \times 10^{10}\text{ V}$**.

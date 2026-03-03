## 1. Vector Algebra

Given two vectors in 3D space: $\vec{a} = [2, 1, -3]$ and $\vec{b} = [4, -2, 1]$.

**a) The magnitude of each vector.**

The magnitude of a vector $\vec{v} = [x, y, z]$ is given by $|\vec{v}| = \sqrt{x^2 + y^2 + z^2}$.

- $|\vec{a}| = \sqrt{2^2 + 1^2 + (-3)^2} = \sqrt{4 + 1 + 9} = \sqrt{14}$
- $|\vec{b}| = \sqrt{4^2 + (-2)^2 + 1^2} = \sqrt{16 + 4 + 1} = \sqrt{21}$

**b) The dot product $\vec{a} \cdot \vec{b}$.**

The dot product is given by $\vec{a} \cdot \vec{b} = a_x b_x + a_y b_y + a_z b_z$.
- $\vec{a} \cdot \vec{b} = (2 \cdot 4) + (1 \cdot (-2)) + ((-3) \cdot 1) = 8 - 2 - 3 = 3$

**c) The cross product $\vec{a} \times \vec{b}$.**

The cross product is computed using the determinant of a matrix with standard basis vectors $\mathbf{i}, \mathbf{j}, \mathbf{k}$:

$$
\vec{a} \times \vec{b} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & 1 & -3 \\ 4 & -2 & 1 \end{vmatrix}
= \mathbf{i}(1 \cdot 1 - (-3)(-2)) - \mathbf{j}(2 \cdot 1 - (-3) \cdot 4) + \mathbf{k}(2(-2) - 1 \cdot 4)
$$

- $\vec{a} \times \vec{b} = \mathbf{i}(1 - 6) - \mathbf{j}(2 + 12) + \mathbf{k}(-4 - 4) = -5\mathbf{i} - 14\mathbf{j} - 8\mathbf{k} = [-5, -14, -8]$

**d) The angle between vectors $\vec{a}$ and $\vec{b}$.**

We use the formula $\vec{a} \cdot \vec{b} = |\vec{a}||\vec{b}|\cos\theta$.
- $\cos\theta = \frac{\vec{a} \cdot \vec{b}}{|\vec{a}||\vec{b}|} = \frac{3}{\sqrt{14}\sqrt{21}} = \frac{3}{\sqrt{294}}$
- $\theta = \arccos\left(\frac{3}{\sqrt{294}}\right) \approx 79.9^\circ$ (or $1.39$ radians)
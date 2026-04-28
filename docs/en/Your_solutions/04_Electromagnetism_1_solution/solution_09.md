# 9. Vector Lorentz Force

**Problem:**
A proton moves with a velocity $\vec{v} = (2\hat{i} - 4\hat{j} + \hat{k}) \text{ m/s}$ in a region where the magnetic field is $\vec{B} = (\hat{i} + 2\hat{j} - \hat{k}) \text{ T}$. What is the magnitude of the magnetic force this charge experiences?

**Solution:**
We are given:

* Proton charge: $q \approx 1.6 \times 10^{-19}\text{ C}$
* Velocity vector: $\vec{v} = 2\hat{i} - 4\hat{j} + \hat{k}$
* Magnetic field vector: $\vec{B} = \hat{i} + 2\hat{j} - \hat{k}$

The magnetic Lorentz force vector is given by the cross product of velocity and magnetic field vectors:
$$ \vec{F} = q(\vec{v} \times \vec{B}) $$

**1. Calculate the cross product $\vec{v} \times \vec{B}$**
We can use the determinant of a $3 \times 3$ matrix to find the cross product:

$$ \vec{v} \times \vec{B} = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ v_x & v_y & v_z \\ B_x & B_y & B_z \end{vmatrix} = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ 2 & -4 & 1 \\ 1 & 2 & -1 \end{vmatrix} $$

Expand the determinant:

$$ \vec{v} \times \vec{B} = \hat{i} \begin{vmatrix} -4 & 1 \\ 2 & -1 \end{vmatrix} - \hat{j} \begin{vmatrix} 2 & 1 \\ 1 & -1 \end{vmatrix} + \hat{k} \begin{vmatrix} 2 & -4 \\ 1 & 2 \end{vmatrix} $$

$$ \vec{v} \times \vec{B} = \hat{i} ((-4)(-1) - (1)(2)) - \hat{j} ((2)(-1) - (1)(1)) + \hat{k} ((2)(2) - (-4)(1)) $$

$$ \vec{v} \times \vec{B} = \hat{i} (4 - 2) - \hat{j} (-2 - 1) + \hat{k} (4 + 4) $$

$$ \vec{v} \times \vec{B} = 2\hat{i} + 3\hat{j} + 8\hat{k} $$

**2. Calculate the magnitude of the cross product**
$$ |\vec{v} \times \vec{B}| = \sqrt{2^2 + 3^2 + 8^2} $$

$$ |\vec{v} \times \vec{B}| = \sqrt{4 + 9 + 64} = \sqrt{77} \approx 8.775\text{ m}\cdot\text{T/s} $$

**3. Calculate the magnitude of the force**
The magnitude of the force is $F = q |\vec{v} \times \vec{B}|$:
$$ F = (1.6 \times 10^{-19}\text{ C}) \times \sqrt{77}\text{ m}\cdot\text{T/s} $$

$$ F \approx (1.6 \times 10^{-19}) \times 8.775 $$

$$ F \approx 14.04 \times 10^{-19}\text{ N} = 1.404 \times 10^{-18}\text{ N} $$

**Answer:**
The magnitude of the magnetic force the proton experiences is approximately **$1.4 \times 10^{-18}\text{ N}$**.

# Solution 3: Biot-Savart Law

## Problem Statement
A small segment of a line wire of length $0.1 \text{ m}$ carries a current of $3 \text{ A}$. The segment is located at a distance of $0.2 \text{ m}$ from a point $P$. Calculate the magnetic field at point $P$ due to this current segment (assume the segment is perpendicular to the line connecting it to point $P$).

## Step-by-Step Solution

**1. Recall the Biot-Savart Law:**

The magnitude of the magnetic field $dB$ produced by a small segment of wire of length $dl$ carrying current $I$ at a point located at a distance $r$ is given by:

$$ dB = \frac{\mu_0 I dl \sin\theta}{4\pi r^2} $$

where:

* $\mu_0 = 4\pi \times 10^{-7} \text{ T}\cdot\text{m/A}$ is the vacuum permeability.
* $\theta$ is the angle between the current element vector $d\mathbf{l}$ and the position vector $\mathbf{r}$ pointing from the element to the point.

**2. Identify the given values:**

* Current, $I = 3 \text{ A}$
* Length of the wire segment, $dl = 0.1 \text{ m}$
* Distance to point $P$, $r = 0.2 \text{ m}$
* Angle, $\theta = 90^\circ$ (since the segment is perpendicular to the line connecting it to point $P$).

**3. Calculate the magnetic field:**

Since $\sin(90^\circ) = 1$, the formula simplifies to:

$$ B \approx dB = \frac{\mu_0 I dl}{4\pi r^2} $$

Substitute the known values into the equation:

$$ B = \frac{(4\pi \times 10^{-7} \text{ T}\cdot\text{m/A}) (3 \text{ A}) (0.1 \text{ m})}{4\pi (0.2 \text{ m})^2} $$

$$ B = 10^{-7} \times \frac{0.3}{0.04} \text{ T} $$

$$ B = 10^{-7} \times 7.5 \text{ T} $$

$$ B = 7.5 \times 10^{-7} \text{ T} = 0.75 \text{ μT} $$

**Final Answer:**
The magnetic field at point $P$ due to this current segment is **$7.5 \times 10^{-7} \text{ T}$** (or $0.75 \text{ μT}$).

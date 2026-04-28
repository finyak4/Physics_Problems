# 3. Electrostatic Equilibrium

**Problem:**
Find the equilibrium position for a charge $q_3 = +1\text{C}$ placed on the line between a charge $q_1 = +4\text{C}$ and a charge $q_2 = +9\text{C}$, which are separated by a distance of $2\text{ m}$.

**Solution:**
Let the distance between $q_1$ and $q_2$ be $d = 2\text{ m}$.
Let the position of $q_3$ be $x$ meters away from $q_1$. Since it sits between the charges (for the repulsive forces from the two positive charges to roughly oppose each other, $q_3$ must lie within the segment), its distance to $q_2$ will be $(d - x) = (2 - x)$ meters.

For the charge $q_3$ to be in electrostatic equilibrium, the net force acting on it must be zero. This means the repulsive force exerted by $q_1$ on $q_3$ must be equal in magnitude and opposite in direction to the repulsive force exerted by $q_2$ on $q_3$.

$$ |\vec{F}_{13}| = |\vec{F}_{23}| $$

Using Coulomb's law:
$$ k \frac{|q_1| |q_3|}{x^2} = k \frac{|q_2| |q_3|}{(2 - x)^2} $$

Both $k$ and $|q_3|$ are on both sides of the equation and are non-zero, so we can cancel them out:
$$ \frac{|q_1|}{x^2} = \frac{|q_2|}{(2 - x)^2} $$

Substitute the values of the charges ($|q_1| = 4$, $|q_2| = 9$):
$$ \frac{4}{x^2} = \frac{9}{(2 - x)^2} $$

Take the square root of both sides (since $x$ represents distance between charges, $0 < x < 2$):
$$ \frac{2}{x} = \frac{3}{2 - x} $$

Cross-multiply to solve for $x$:
$$ 2(2 - x) = 3x $$
$$ 4 - 2x = 3x $$
$$ 4 = 5x $$
$$ x = \frac{4}{5} = 0.8\text{ m} $$

**Answer:**
The equilibrium position for the charge $q_3$ is **$0.8\text{ m}$ away from the $+4\text{C}$ charge** (and $1.2\text{ m}$ away from the $+9\text{C}$ charge).

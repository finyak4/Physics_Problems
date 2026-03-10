## 10. Kinematics

$\vec{r}(t) = (a \cos(\omega t), b \sin(\omega t), bt)$

**Step-by-step solution:**
1. **Equation of trajectory (a):**
   The coordinates are $x = a \cos(\omega t), y = b \sin(\omega t), z = bt$.
   Notice that $\frac{x^2}{a^2} + \frac{y^2}{b^2} = \cos^2(\omega t) + \sin^2(\omega t) = 1$.
   The projection onto the $xy$-plane is an ellipse. Since $z = bt$, $z$ grows linearly with time. The trajectory is an **elliptical helix** winding around the $z$-axis.
2. **Path length (b):**
   First, find the velocity vector $\vec{v}(t) = \frac{d\vec{r}}{dt}$.
   $\vec{v}(t) = \left( -a\omega \sin(\omega t), b\omega \cos(\omega t), b \right)$
   Find its magnitude $|\vec{v}(t)|$:
   $|\vec{v}(t)| = \sqrt{(-a\omega \sin(\omega t))^2 + (b\omega \cos(\omega t))^2 + b^2} = \sqrt{a^2\omega^2 \sin^2(\omega t) + b^2\omega^2 \cos^2(\omega t) + b^2}$
   The path length $L$ from $0$ to $t_0$ is the integral of the speed:
   $L = \int_{0}^{t_0} \sqrt{a^2\omega^2 \sin^2(\omega t) + b^2\omega^2 \cos^2(\omega t) + b^2} dt$
   If $a \neq b$, this is an incomplete elliptic integral of the second kind.
3. **Special cases (c):**
   If $a = b$ (the ellipse becomes a circle), the speed simplifies significantly:
   $|\vec{v}(t)| = \sqrt{a^2\omega^2(\sin^2(\omega t) + \cos^2(\omega t)) + b^2} = \sqrt{a^2\omega^2 + b^2}$
   Thus, speed is constant. The path length becomes:
   $L = \int_{0}^{t_0} \sqrt{a^2\omega^2 + b^2} dt = t_0 \sqrt{a^2\omega^2 + b^2}$
   The trajectory in this case is a standard circular helix.

## 2. Range Optimization

Show analytically that the maximum range $R(\theta)=\frac{v_0^2 \sin(2\theta)}{g}$ is achieved at a launch angle of $45^\circ$.

**Step-by-step solution:**
1. To find the maximum of a function with respect to $\theta$, take the first derivative and set it to zero:
   $\frac{dR}{d\theta} = \frac{d}{d\theta} \left( \frac{v_0^2}{g} \sin(2\theta) \right) = \frac{v_0^2}{g} \cdot 2\cos(2\theta) = 0$
2. Since $\frac{2v_0^2}{g}$ is a non-zero constant, we must have:
   $\cos(2\theta) = 0$
3. The principal solution for realistic launch angles ($0 \le \theta \le 90^\circ$) is:
   $2\theta = 90^\circ \implies \theta = 45^\circ$
4. To verify it's a maximum, take the second derivative:
   $\frac{d^2R}{d\theta^2} = -\frac{4v_0^2}{g} \sin(2\theta)$
   At $\theta = 45^\circ$, $\frac{d^2R}{d\theta^2} = -\frac{4v_0^2}{g} < 0$. Since it's negative, $\theta = 45^\circ$ indeed gives the maximum range.

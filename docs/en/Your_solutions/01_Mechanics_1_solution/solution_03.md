## 3. Path Intersection

Paths: $A(t) = (2+t, 8-3t)$ and $B(t) = (2t-1, 2t+2)$.

**Step-by-step solution:**
1. **Intersection:** For paths to intersect (collide), they must be at the same place at the *same* time $t$.
   Equate the $x$-coordinates: $2 + t = 2t - 1 \implies t = 3$
2. Check the $y$-coordinates at $t = 3$:
   $A_y(3) = 8 - 3(3) = -1$
   $B_y(3) = 2(3) + 2 = 8$
   Since $-1 \neq 8$, the paths **do not intersect** (they don't collide).
3. **Minimum distance:**
   The square of the distance between them is:
   $D^2(t) = (A_x - B_x)^2 + (A_y - B_y)^2 = (2+t - (2t-1))^2 + (8-3t - (2t+2))^2$
   $D^2(t) = (3 - t)^2 + (6 - 5t)^2$
   $D^2(t) = (9 - 6t + t^2) + (36 - 60t + 25t^2) = 26t^2 - 66t + 45$
4. To find the minimum distance, minimize $D^2(t)$:
   $\frac{d(D^2)}{dt} = 52t - 66 = 0 \implies t = \frac{66}{52} = \frac{33}{26} \approx 1.27 \text{ s}$
5. Substitute $t = \frac{33}{26}$ back to find $D$:
   $D = \sqrt{26\left(\frac{33}{26}\right)^2 - 66\left(\frac{33}{26}\right) + 45} = \sqrt{\frac{1089 - 2178 + 1170}{26}} = \sqrt{\frac{81}{26}} = \frac{9}{\sqrt{26}} \approx 1.765$

**Answer:** They do not collide. Minimum distance is $9/\sqrt{26} \approx 1.765$ at time $t = 33/26 \approx 1.27\text{ s}$.
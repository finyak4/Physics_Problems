# 7. Dynamics with Friction

## Problem Statement
A 5 kg block is placed on a 10 kg block. A horizontal force of 45 N is applied to the 10 kg block, and the 5 kg block is tied to the wall. The coefficient of kinetic friction between all moving surfaces is 0.2. Find the acceleration of the 10 kg block.

## Step-by-Step Solution

1. **Identify the forces on the 10 kg block ($m_2 = 10 \text{ kg}$):**

   - The applied horizontal force $F = 45 \text{ N}$ acts to the right.
   - The friction force from the floor $f_{k2}$ acts to the left.
   - The friction force from the 5 kg block ($m_1 = 5 \text{ kg}$) above it $f_{k1}$ acts to the left.

2. **Calculate the normal forces:**

   - For the 5 kg block, the normal force $N_1$ between the two blocks is just the weight of the top block:
     $$ N_1 = m_1 g = 5 \times 9.81 = 49.05 \text{ N} $$
   - For the 10 kg block, the normal force $N_2$ between the bottom block and the floor must support both blocks:
     $$ N_2 = (m_1 + m_2) g = (5 + 10) \times 9.81 = 15 \times 9.81 = 147.15 \text{ N} $$

3. **Calculate the friction forces:**

   - Friction between the 5 kg block and the 10 kg block ($f_{k1}$):
     $$ f_{k1} = \mu_k N_1 = 0.2 \times 49.05 = 9.81 \text{ N} $$
   - Friction between the 10 kg block and the floor ($f_{k2}$):
     $$ f_{k2} = \mu_k N_2 = 0.2 \times 147.15 = 29.43 \text{ N} $$

4. **Apply Newton's Second Law to the 10 kg block:**

   - The net force on the 10 kg block is $F_{\text{net}} = F - f_{k1} - f_{k2}$.
   - According to Newton's Second Law:
     $$ F_{\text{net}} = m_2 a_2 $$
   - Substituting the forces:
     $$ F - f_{k1} - f_{k2} = m_2 a_2 $$

5. **Solve for the acceleration $a_2$:**

   $$ 45 - 9.81 - 29.43 = 10 \times a_2 $$
   $$ 45 - 39.24 = 10 a_2 $$
   $$ 5.76 = 10 a_2 \implies a_2 = 0.576 \text{ m/s}^2 $$

6. **Conclusion:**
   The acceleration of the 10 kg block is **$0.576 \text{ m/s}^2$**.

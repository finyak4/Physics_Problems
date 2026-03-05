# Comprehensive Review of Mechanics (Chapters 2–5)

Physics builds from the ground up: before we can ask *why* things move (forces), we must rigorously define *how* they move (kinematics). This text compresses the core concepts of Mechanics from University Physics (Chapters 2 to 5) into an intensive, high-yield reading. It replaces hundreds of pages of textbooks with a 20-minute conceptual deep-dive, complete with problem-solving examples.

---

## Chapter 2: Kinematics in One Dimension

The fundamental leap from standard high school physics to university physics is recognizing that motion is deeply rooted in **calculus**. Algebraic formulas are simply special cases of integrals.

### 1. Position, Velocity, and Acceleration
Everything begins with the position function, $x(t)$, which tracks where an object is along a line at any given moment.

* **Velocity ($v_x$):** The rate of change of position—the first derivative of $x(t)$.
  $$ v_x = \frac{dx}{dt} $$
* **Acceleration ($a_x$):** The rate of change of velocity—the first derivative of $v_x(t)$, or alternatively, the second derivative of $x(t)$.
  $$ a_x = \frac{dv_x}{dt} = \frac{d^2x}{dt^2} $$

> **The Deep Concept:** If you have $a(t)$, you can find velocity by integrating. If you have $v(t)$, you integrate to find position. *Always add the constants of integration*: your initial velocity ($v_{0x}$) and initial position ($x_0$).
> $$ v_x(t) = v_{0x} + \int_0^t a_x(t) dt $$
> $$ x(t) = x_0 + \int_0^t v_x(t) dt $$

#### Example 1: Calculus-Based Motion

An object moves such that its position is $x(t) = 2.0t^3 - 5.0t$.

* **Find velocity:** $v_x(t) = \frac{dx}{dt} = 6.0t^2 - 5.0$
* **Find acceleration:** $a_x(t) = \frac{dv_x}{dt} = 12.0t$

* *Conclusion:* This is **not** constant acceleration (it varies over time $t$). You cannot use standard kinematic formulas here; you must rely on calculus!

### 2. Constant Acceleration: The "Big Four" Equations
When (and *only* when) acceleration is **constant**, evaluating the calculus integrals yields the standard kinematic equations:

1. **Final velocity at time 𝑡 (Velocity vs. Time):** 

   $v_x = v_{0x} + a_xt$

2. **Position at time 𝑡 (Position vs. Time):** 

   $x = x_0 + v_{0x}t + \frac{1}{2}a_xt^2$

3. **Velocity when you know displacement but don’t know time:** 

   $v_x^2 = v_{0x}^2 + 2a_x(x - x_0)$

4. **Position when you don't know acceleration (using Average Velocity):** 

   $x - x_0 = \left(\frac{v_{0x} + v_x}{2}\right)t$

#### Example 2: Stopping Distance
A car traveling at $30 \text{ m/s}$ slams on the brakes, producing a steady deceleration of $5 \text{ m/s}^2$. How far does it go before stopping?

* **Given:** $v_{0x} = 30 \text{ m/s}$, $v_x = 0 \text{ m/s}$ (it stops), $a_x = -5 \text{ m/s}^2$.

* **Unknown:** $\Delta x = x - x_0$.

* **Analysis:** Use equation #3 to bypass time entirely.
  $$ 0 = (30)^2 + 2(-5)(\Delta x) \implies 10\Delta x = 900 \implies \Delta x = 90 \text{ m} $$

### 3. Free Fall
Free fall is simply 1D kinematics where a constant acceleration is provided by Earth's gravity: $g = 9.8 \text{ m/s}^2$.

* **The Trap:** $g$ is a positive magnitude. If you define "up" as the positive y-direction, $a_y = -g = -9.8 \text{ m/s}^2$.
* **The Turning Point:** At the highest point of a thrown ball, its velocity is instantaneously zero ($v_y = 0$), but **its acceleration is still $-9.8 \text{ m/s}^2$**. If acceleration were zero at the top, the ball would hover there forever!

---

## Chapter 3: Kinematics in Two and Three Dimensions

Now we move from a simple line to a plane or full 3D space. The master key here is **Vector Independence**: Motion in the x-direction is completely independent of motion in the y-direction. They are separate 1D problems linked by only one shared variable: **time ($t$)**.

### 1. Position, Velocity, and Acceleration Vectors
In 3D, we use unit vectors $\hat{i}$, $\hat{j}$, and $\hat{k}$.

* Position vector: $\vec{r} = x\hat{i} + y\hat{j} + z\hat{k}$

* Velocity vector: $\vec{v} = v_x\hat{i} + v_y\hat{j} + v_z\hat{k} = \frac{dx}{dt}\hat{i} + \frac{dy}{dt}\hat{j} + \frac{dz}{dt}\hat{k}$

### 2. Projectile Motion
When an object is launched freely into the air, it experiences gravity pulling it down (Y-axis), but *nothing* pushing it horizontally (X-axis, assuming we ignore air resistance).
Thus, we split into two simultaneous 1D problems:

* **X-axis (Horizontal):** Constant velocity. $a_x = 0$.
  $$ x = x_0 + (v_0 \cos\theta)t $$
* **Y-axis (Vertical):** Free fall. $a_y = -g$.
  $$ y = y_0 + (v_0 \sin\theta)t - \frac{1}{2}gt^2 $$
  $$ v_y = v_0 \sin\theta - gt $$

> **Exam Strategy:** In projectile motion, use the Y-axis equations to find *time* (e.g., when does it hit the ground, when $y=0$?), and then plug that $t$ into the X-axis equation to find the *range* (how far it flew horizontally).

#### Example 3: Firing a Projectile Horizontally
A cannonball is fired strictly horizontally ($v_{0y} = 0$, $v_{0x} = 20 \text{ m/s}$) from a $49 \text{ m}$ high cliff. Where does it land relative to the base of the cliff?

1. **Find time in air (Y-axis):** Let the base of the cliff be $y=0$, so $y_0 = 49 \text{ m}$.
   $$ y = y_0 + v_{0y}t - \frac{1}{2}gt^2 \implies 0 = 49 + 0 - 4.9t^2 $$
   $$ 4.9t^2 = 49 \implies t^2 = 10 \implies t \approx 3.16 \text{ s} $$
2. **Find horizontal range (X-axis):**
   $$ x = x_0 + v_{0x}t \implies x = 0 + (20)(3.16) \approx 63.2 \text{ m} $$

### 3. Uniform Circular Motion
When moving in a circle at a constant speed $v$, the velocity vector's *magnitude* is constant, but its *direction* is constantly changing. Because velocity is a vector, any change means **it is accelerating**.

* **Centripetal Acceleration ($a_{rad}$):** This acceleration always points directly toward the center of the circle.
  $$ a_{rad} = \frac{v^2}{R} $$
The time it takes to complete one revolution is the period $T = \frac{2\pi R}{v}$. Therefore, $a_{rad}$ can also be written in terms of period: $a_{rad} = \frac{4\pi^2 R}{T^2}$.

### 4. Angular Velocity, Angular Acceleration, and Non-Uniform Circular Motion
While uniform circular motion deals with constant speed, an object can also speed up or slow down as it moves in a circle. In these cases, we evaluate motion using angles ($\theta$, measured in radians) rather than linear distance:

* **Angular Velocity ($\omega$):** The rate of change of the angle with respect to time.
  $$ \omega = \frac{d\theta}{dt} $$
  It relates directly to the linear tangential speed $v$ by the equation: $v = \omega R$. (Since $a_{rad} = \frac{v^2}{R}$, this gives another common form for centripetal force: **$a_{rad} = \omega^2 R$**).

* **Angular Acceleration ($\alpha$):** The rate of change of angular velocity.
  $$ \alpha = \frac{d\omega}{dt} = \frac{d^2\theta}{dt^2} $$
  When $\alpha \neq 0$, the object has a **tangential acceleration ($a_{tan}$)** along the edge of the circle:
  $$ a_{tan} = \alpha R $$
  Unlike centripetal acceleration (which strictly changes the *direction* of the movement), tangential acceleration strictly changes the *speed* of the rotation. Total acceleration is the vector sum: $\vec{a} = \vec{a}_{rad} + \vec{a}_{tan}$.

### 5. Relative Velocity
Velocities depend on your frame of reference. If a Patient walks at $v_{P/T}$ (Patient relative to Train) on a moving Train traveling at $v_{T/G}$ (Train relative to Ground), velocity to the Ground $v_{P/G}$ is:

$$ 
\vec{v}_{P/G} = \vec{v}_{P/T} + \vec{v}_{T/G}
$$

To avoid getting lost, use the subscript canceling trick: the 'T' in the middle adjacent subscripts "cancels" out to leave $P/G$.

#### Example 4: Crossing a River
A boat points straight across a river and travels at $4.0 \text{ m/s}$ relative to the water ($v_{B/W}$). The river flows parallel to the banks at $3.0 \text{ m/s}$ relative to the ground ($v_{W/G}$). What is the speed of the boat relative to the ground ($v_{B/G}$)?

* **Vector Equation:** $\vec{v}_{B/G} = \vec{v}_{B/W} + \vec{v}_{W/G}$

* **Analysis:** These two vectors are perpendicular to each other. The boat is moving across the river 
(Y-axis), while the river flows downstream (X-axis).

* Because they are perpendicular, we use the Pythagorean theorem to find the magnitude of the velocity relative to the ground:
  $$ v_{B/G} = \sqrt{(4.0)^2 + (3.0)^2} = \sqrt{16 + 9} = \sqrt{25} = 5.0 \text{ m/s} $$
* The boat travels diagonally relative to a person standing on the shore.

---

## Chapter 4: Newton's Laws of Motion

Kinematics merely describes *how* things move. Dynamics describes *why*. The "why" is **Force**.

### 1. Newton's First Law (Inertia)
*An object at rest stays at rest, and an object in uniform motion (constant velocity in a straight line) stays in uniform motion unless acted upon by a net external force.*

* **The Deep Concept:** A net force of zero $\left(\sum \vec{F} = 0\right)$ does *not* strictly mean an object is stationary. It simply means the object is **not accelerating** ($\vec{a} = 0$, making $\vec{v}$ constant). A probe cruising through deep space at $10,000 \text{ m/s}$ with its engines off has a net force of exactly zero.

### 2. Newton's Second Law
This is the heart of classical mechanics. It relates the net external force on a mass to its acceleration. It is a vector equation, meaning you must solve it independently for each axis.
$$ \sum \vec{F} = m\vec{a} $$
Which splits into: $\sum F_x = ma_x$, $\sum F_y = ma_y$, and $\sum F_z = ma_z$.

* **Mass ($m$)** is an object's innate resistance to being accelerated (its inertia). It is measured in kg, and is a scalar. A $10 \text{ kg}$ block is $10 \text{ kg}$ on Earth, on the Moon, or in deep space.
* **Weight ($W$)** is the gravitational force acting on that mass: $W = mg$. Measured in Newtons (N). Your weight absolutely changes depending on local gravity.

### 3. Newton's Third Law
*If Body A exerts a force on Body B, then Body B exerts an equal and opposite force on Body A.*
$$ \vec{F}_{A \text{ on } B} = -\vec{F}_{B \text{ on } A} $$

* **The Trap:** Action-reaction pairs **never** act on the same object! Thus, they never cancel each other out in a single free-body diagram.
* *Classic Example:* A book resting on a table. Gravity pulls down on the book; the table's Normal force pushes up on the book. Are they a 3rd Law pair? **No.** They both act on the book! The actual 3rd law pair to the Earth pulling down on the book is the **Book pulling up on the Earth** with the exact same gravitational force!

---

## Chapter 5: Applying Newton's Laws

This chapter transforms theories into applied methodology. The absolute most critical tool in your physics arsenal from here on out is the **Free-Body Diagram (FBD)**.

### Master Strategy for Dynamics Problems
1. **Sketch the scenario.**
2. **Draw a Free-Body Diagram for EACH object.** Represent the object as a mere dot. Draw arrows for forces acting *on* the object (Weight, Normal force, Tension, Friction). Do *not* draw velocities or accelerations here.
3. **Choose a Coordinate System.**
   * *Pro-Tip:* Always set one axis strictly in the direction of acceleration. If a block is sliding down a ramp, **tilt your axes**. Make the ramp surface the X-axis. This guarantees $a_y = 0$, saving you from horrific simultaneous equations.
4. **Break Forces into Components.** Use sine and cosine trigonometry to break any diagonal forces into neat X and Y pieces.
5. **Apply Newton's Second Law:** Write out $\sum F_x = ma_x$ and $\sum F_y = ma_y$, and solve algebraically.

### 1. Particles in Equilibrium ($\sum \vec{F} = 0$)
When an object is stationary or moving at a constant velocity, its acceleration is zero. Therefore, $\sum F_x = 0$ and $\sum F_y = 0$.

#### Example 5: A Hanging Sign
A $10 \text{ kg}$ sign hangs statically from a knot connecting two ropes. Rope 1 goes exactly horizontal to a left wall. Rope 2 extends rightward and upwards, attaching to the ceiling at an angle of $45^\circ$ above the horizontal. Find the tension in Rope 2 ($T_2$).
1. **Forces on the Knot:** 
   * Weight ($W = 10 \times 9.8 = 98 \text{ N}$, straight down).
   * Tension 1 ($T_1$, straight left).
   * Tension 2 ($T_2$, pulling up and right at $45^\circ$).
2. **Y-axis equation:** $T_2$ has an upward component of $T_2 \sin(45^\circ)$.
   $$ \sum F_y = T_2 \sin(45^\circ) - W = 0 \implies T_2 \sin(45^\circ) = 98 $$
   $$ T_2 = \frac{98}{0.707} \approx 138.6 \text{ N} $$
3. **X-axis equation:** $T_2$'s rightward component perfectly battles $T_1$'s leftward pull.
   $$ \sum F_x = T_2 \cos(45^\circ) - T_1 = 0 \implies T_1 = 138.6 \times 0.707 \approx 98 \text{ N} $$

### 2. Friction
Friction opposes **relative slipping** between two surfaces.

* **Static Friction ($f_s$):** Keeps an object from moving. It is a "smart" shifting force; it provides exactly as much outward force as needed to prevent motion, up to a structural breaking point.
  $$ f_s \le \mu_s n $$
  (Where $\mu_s$ is the coefficient of static friction, and $n$ is Normal force).
* **Kinetic Friction ($f_k$):** The constant friction experienced once slipping occurs.
  $$ f_k = \mu_k n $$

> **The Deep Concept:** $\mu_s > \mu_k$. It takes a harder initial push to break a heavy couch loose than it does to keep it sliding across the room once it's in motion.

#### Example 6: Sliding Down a Ramp with Friction
A $2.0 \text{ kg}$ block is placed on a $30^\circ$ incline. The coefficient of kinetic friction $\mu_k = 0.20$. What is its acceleration down the ramp?
1. **Axes:** Tilt the X-axis parallel down the ramp. Y-axis is perpendicular to the ramp.
2. **Components of Gravity (Weight):**
   * $W_x = mg \sin(30^\circ)$ (Pulling it down the ramp's face)
   * $W_y = mg \cos(30^\circ)$ (Pushing it into the ramp's surface)
3. **Y-axis (No vertical acceleration relative to the ramp):**
   $$ \sum F_y = n - W_y = 0 \implies n = mg \cos(30^\circ) $$
4. **X-axis (Motion down the ramp):**
   $$ \sum F_x = W_x - f_k = ma_x $$
   * Substitute $f_k = \mu_k n$, turning that into $\mu_k (mg \cos(30^\circ))$.
   $$ mg \sin(30^\circ) - \mu_k mg \cos(30^\circ) = ma_x $$
   * Divide by $m$ (mass cancels! Weight doesn't dictate how fast things slide):
   $$ a_x = g(\sin(30^\circ) - \mu_k \cos(30^\circ)) $$
   $$ a_x = 9.8 (0.500 - 0.20 \times 0.866) = 9.8 (0.500 - 0.173) = 9.8 (0.327) \approx 3.20 \text{ m/s}^2 $$

### 3. Dynamics of Circular Motion
In Chapter 3, we established $a_{rad} = v^2/R$. Because there is an inward acceleration, Newton's Second Law demands there be an actual inward **net force**.
$$ \sum F_{rad} = m a_{rad} = m\frac{v^2}{R} $$

* **The Trap:** "Centripetal force" is NOT a new, magical force you invent on your Free-Body Diagram. It is merely a *job description* given to whatever real forces (Tension, Gravity, Friction) happen to be pointing toward the center of the circle.

#### Example 7: An Unbanked Curve
A $1000 \text{ kg}$ car rounds a flat, unbanked curve of radius $50 \text{ m}$ at $15 \text{ m/s}$. What minimum coefficient of static friction $\mu_s$ is required to keep it from skidding outward? (Note: It is *static* friction giving you grip during a clean turn, as the tires are not actively slipping sideways across the asphalt!)
* **Forces:** Gravity (down), Normal force (up), Static friction (pointing inward toward the center of the curve).
* **Y-axis:** $n - mg = 0 \implies n = 1000 \times 9.8 = 9800 \text{ N}$
* **X-axis (Radial direction):** The only force pointing to the center is static friction.
  $$ \sum F_{rad} = f_s = m\frac{v^2}{R} $$
  $$ f_s = 1000 \times \frac{15^2}{50} = 1000 \times \frac{225}{50} = 4500 \text{ N} $$
* We know maximum static friction is $f_s = \mu_s n$. To just barely keep the car from sliding at this threshold speed, set $f_s$ to its absolute maximum:
  $$ 4500 = \mu_s (9800) \implies \mu_s = \frac{4500}{9800} \approx 0.46 $$
You need at least $\mu_s = 0.46$ between the tires and the road to make this turn safely.

---

# 7. Cyclotron Motion

**Problem:**
An electron is accelerated from rest through a potential difference of $5000\text{ V}$. It then enters a region of uniform magnetic field B = $0.1\text{ T}$, perpendicular to its velocity. What is the radius of the circular path it will follow?

**Solution:**
We are given:
* Potential difference: $V = 5000\text{ V}$
* Magnetic field: $B = 0.1\text{ T}$
* Charge of electron: $q = 1.6 \times 10^{-19}\text{ C}$
* Mass of electron: $m = 9.1 \times 10^{-31}\text{ kg}$

**1. Determine the velocity of the electron**
The electron is accelerated by the electric field, so its potential energy is converted into kinetic energy:
$$ K = qV $$
$$ \frac{1}{2} m v^2 = qV $$
$$ v = \sqrt{\frac{2qV}{m}} $$

Substitute the given values:
$$ v = \sqrt{\frac{2(1.6 \times 10^{-19}\text{ C})(5000\text{ V})}{9.1 \times 10^{-31}\text{ kg}}} $$
$$ v = \sqrt{\frac{1.6 \times 10^{-15}}{9.1 \times 10^{-31}}} = \sqrt{1.758 \times 10^{15}} = \sqrt{17.58 \times 10^{14}} $$
$$ v \approx 4.19 \times 10^7\text{ m/s} $$

**2. Determine the radius of the circular path**
When the electron enters the magnetic field perpendicular to its velocity, the magnetic force provides the centripetal force required for circular motion:
$$ F_B = F_c $$
$$ qvB = \frac{mv^2}{r} $$

Solving for the radius $r$:
$$ r = \frac{mv}{qB} $$

We can either plug in the computed velocity $v$, or substitute the expression for $v$ to compute it in one step:
$$ r = \frac{m}{qB} \sqrt{\frac{2qV}{m}} = \frac{1}{B} \sqrt{\frac{2mV}{q}} $$

Let's plug in the numbers using the full formula:
$$ r = \frac{1}{0.1} \sqrt{\frac{2(9.1 \times 10^{-31})(5000)}{1.6 \times 10^{-19}}} $$
$$ r = 10 \sqrt{\frac{9.1 \times 10^{-27}}{1.6 \times 10^{-19}}} = 10 \sqrt{5.6875 \times 10^{-8}} $$
$$ r = 10(2.385 \times 10^{-4}) $$
$$ r \approx 2.385 \times 10^{-3}\text{ m} = 2.385\text{ mm} $$

**Answer:**
The radius of the circular path is approximately **$2.39\text{ mm}$** (or $2.385 \times 10^{-3}\text{ m}$).

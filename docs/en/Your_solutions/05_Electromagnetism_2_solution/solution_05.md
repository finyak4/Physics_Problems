# Solution 5: Energy Stored by charge in a capacitor

## Problem Statement

We have a parallel-plate capacitor with the following parameters:

* $S = 0.02\,\mathrm{m^2}$
* $d = 5\,\mathrm{mm}$
* $U = 500\,\mathrm{V}$

We have to:

1. Calculate the capacitance $C$ of the capacitor.
2. Calculate the energy $W$ stored in the capacitor.
3. Calculate the electric field intensity $E$ between the plates.
4. Calculate the force of attraction $F$ between the plates.

## Step-by-Step Solution

First, let's list the knowns in SI units:

* Plate area, $S = 0.02 \text{ m}^2$

* Distance between plates, $d = 5 \text{ mm} = 0.005 \text{ m}$

* Voltage across the plates, $U = 500 \text{ V}$

* Vacuum permittivity, $\epsilon_0 \approx 8.854 \times 10^{-12} \text{ F/m}$ (assuming air/vacuum between the plates).

**1. Calculate the capacitance $C$**

The capacitance of a parallel-plate capacitor is given by:

$$ C = \frac{\epsilon_0 S}{d} $$
Substitute the values:

$$ C = \frac{(8.854 \times 10^{-12} \text{ F/m}) \times (0.02 \text{ m}^2)}{0.005 \text{ m}} $$

$$ C = \frac{1.7708 \times 10^{-13}}{0.005} \text{ F} = 3.5416 \times 10^{-11} \text{ F} \approx 35.4 \text{ pF} $$

**2. Calculate the stored energy $W$**

The energy stored in a capacitor is:

$$ W = \frac{1}{2} C U^2 $$

Substitute the values:

$$ W = \frac{1}{2} (3.5416 \times 10^{-11} \text{ F}) \times (500 \text{ V})^2 $$

$$ W = \frac{1}{2} (3.5416 \times 10^{-11}) \times 250,000 \text{ J} $$

$$ W = 4.427 \times 10^{-6} \text{ J} \approx 4.43 \text{ \mu J} $$

**3. Calculate the electric field intensity $E$**

The magnitude of the uniform electric field between the plates is:

$$ E = \frac{U}{d} $$

Substitute the values:

$$ E = \frac{500 \text{ V}}{0.005 \text{ m}} = 100,000 \text{ V/m} = 10^5 \text{ V/m} $$

**4. Calculate the force of attraction $F$**

The attractive force between the parallel plates of a capacitor is given by:

$$ F = \frac{1}{2} \epsilon_0 E^2 S $$

Substitute the values:

$$ F = \frac{1}{2} (8.854 \times 10^{-12} \text{ F/m}) \times (10^5 \text{ V/m})^2 \times (0.02 \text{ m}^2) $$

$$ F = \frac{1}{2} \times 8.854 \times 10^{-12} \times 10^{10} \times 0.02 \text{ N} $$

$$ F = 8.854 \times 10^{-2} \times 0.01 \text{ N} $$

$$ F = 8.854 \times 10^{-4} \text{ N} $$

Alternatively, the force can also be found using $F = \frac{C U^2}{2d}$.

**Final Answers:**
1. Capacitance, $C \approx 35.4 \text{ pF}$
2. Stored energy, $W \approx 4.43 \text{ \mu J}$
3. Electric field intensity, $E = 10^5 \text{ V/m}$
4. Force of attraction, $F \approx 8.85 \times 10^{-4} \text{ N}$

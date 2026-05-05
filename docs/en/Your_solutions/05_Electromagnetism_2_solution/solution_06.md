# Solution 6: EM Wave Analysis

## Problem Statement
An electromagnetic wave has its electric field component described by $E_y(x,t) = 100 \sin(10^7 x - \omega t) \text{ V/m}$. What is the direction of propagation? What is the wavelength $\lambda$? What is the angular frequency $\omega$? What is the equation for the magnetic field component?

## Step-by-Step Solution

**1. General form of the EM wave equation:**
The given electric field is $E_y(x,t) = E_0 \sin(kx - \omega t)$.
By comparing this to the general form:
* Amplitude of the electric field, $E_0 = 100 \text{ V/m}$
* Wave number, $k = 10^7 \text{ m}^{-1}$

**2. Direction of propagation:**
The phase term is $(kx - \omega t)$. The negative sign between $kx$ and $\omega t$ indicates that the wave is propagating in the **positive $x$-direction** ($+x$).

**3. Calculate the wavelength $\lambda$:**
The wave number $k$ is related to wavelength by $k = \frac{2\pi}{\lambda}$.
$$ \lambda = \frac{2\pi}{k} = \frac{2\pi}{10^7 \text{ m}^{-1}} = 2\pi \times 10^{-7} \text{ m} \approx 6.28 \times 10^{-7} \text{ m} = 628 \text{ nm} $$

**4. Calculate the angular frequency $\omega$:**
The angular frequency is related to the wave number and the speed of light $c \approx 3 \times 10^8 \text{ m/s}$ by the equation $\omega = c k$.
$$ \omega = (3 \times 10^8 \text{ m/s}) \times (10^7 \text{ m}^{-1}) = 3 \times 10^{15} \text{ rad/s} $$

**5. Determine the magnetic field equation:**
* **Amplitude:** The amplitude of the magnetic field $B_0$ is related to the electric field amplitude by $E_0 = c B_0$.
$$ B_0 = \frac{E_0}{c} = \frac{100 \text{ V/m}}{3 \times 10^8 \text{ m/s}} = \frac{1}{3} \times 10^{-6} \text{ T} \approx 3.33 \times 10^{-7} \text{ T} $$
* **Direction:** The direction of wave propagation is given by the cross product of the electric and magnetic fields: $\mathbf{\hat{k}} = \mathbf{\hat{E}} \times \mathbf{\hat{B}}$.
We know the wave propagates in the $+\hat{i}$ ($x$) direction, and the electric field oscillates in the $+\hat{j}$ ($y$) direction.
So, $\hat{i} = \hat{j} \times \mathbf{\hat{B}}$. Since $\hat{j} \times \hat{k} = \hat{i}$, the magnetic field must oscillate in the $+\hat{k}$ ($z$) direction.
* **Equation:** The magnetic field is in phase with the electric field in a vacuum.
$$ B_z(x,t) = B_0 \sin(kx - \omega t) $$
$$ B_z(x,t) = \frac{1}{3} \times 10^{-6} \sin(10^7 x - 3 \times 10^{15} t) \text{ T} $$

**Final Answers:**
* Direction of propagation: **$+x$-direction**
* Wavelength: **$\lambda = 628 \text{ nm}$**
* Angular frequency: **$\omega = 3 \times 10^{15} \text{ rad/s}$**
* Magnetic field equation: **$B_z(x,t) \approx 3.33 \times 10^{-7} \sin(10^7 x - 3 \times 10^{15} t) \text{ T}$**

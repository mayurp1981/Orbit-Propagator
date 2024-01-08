# Orbit-Propagator

High-Fidelity Orbit Propagator

The orbital prediction code is developed based on Cowell's formulation, considering perturbating effects to enhance accuracy. The predictions acknowledge several crucial factors that influence a satellite's orbit, including the Earth's oblateness, atmospheric drag, solar radiation pressure, third-body perturbations (Moon, Sun), Earth Albedo radiation, tides, variations in Earth's magnetic field, and thrust misalignment. These factors, if not considered, can lead to cumulative errors over time. The code particularly focuses on Low Earth Orbits (LEO), where zonal harmonics J2, atmospheric drag, and third-body perturbations play a predominant role. For polar or sun-synchronous orbits, zonal harmonics J3, J4, J5 also exert a significant influence.

Cowell's formulation is chosen for its accuracy and computational efficiency in addressing these perturbations within the two-body problem. The formulation incorporates additional parameters, such as the satellite's ballistic coefficient, determined by mass, area, and atmospheric density, crucial for precision in orbit predictions. Emphasizing the importance of accurate initial Keplerian elements, the code ensures that deviations from these elements are minimized to maintain prediction accuracy. This high-fidelity modeling approach aims to provide precise and reliable predictions by accounting for a comprehensive set of perturbing effects in the satellite's orbital dynamics.

Estimation of Sun vector is based on first principles[1], while estimation of moon is done using `spicypy` library. Atmospheric density is modelled using `pynrlmsise00`.

**Input:**
Classical Orbital Elements

**Output:**
Propagated Orbit using high-fidelity model and error plot between high-fidelity propagated orbit and basic gravity model propagated orbit with ISS OEM File available in Public domain

Google Colab link: https://colab.research.google.com/drive/1iu7aJ5WrMlWwt37sbKtfiqxWXo2xtjfY?usp=sharing

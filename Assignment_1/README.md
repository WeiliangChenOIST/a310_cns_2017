# Assignment 1

### 1. Simple cable
We prepared a simulation `axon_model.py` that simulates the following axon

* Diameter (`diam`) = 1 um and length (`L`) = 10<sup>3</sup> um,
* Capacitance per area (`cm`) = 1 uF/cm<sup>2</sup>,
* Axial resistance (`Ra`) = 150 Ohm cm,
* Passive mechanism (`pas`) with the conductance per area = 5×10<sup>-5</sup> S/cm<sup>2</sup>.

This axon is attached a current injecting electrode at one end (`ic`) that injects 100 pA from t=100 ms.

1. Calculate the theoretical time and space constant of this axon.
2. Run the simulation by `nrngui -python axon_model.py`. From the simulated data, measure the input resistance and membrane time constant. Does the measured time constant match with the theoretical value?
3. Measure the space constant from the simulated data. Does it match with the theoretical value?
4. Draw a similar attenuation curve as Fig. 2.4 in the Koch. By changing the axon length, make several attenuation curves. From these, can you figure out whether this axon have sealed ends or open ends?


### 2. Passive pyramidal neuron
We prepared a simulation of a cortical pyramidal neuron with a passive membrane, `r18_1.py`.

1. Describe how you can compute the transfer resistance (Equation 3.19 in the Koch) by using this simulation.
2. By using the method, measure the transfer resistance for several locations, and verify the symmetry (Equation 3.27), positivity (Equation 3.28), and transitivy (Equation 3.29) property.
3. Make a sharp current injection (about 1ms duration) at one distal point in a apical dendrite, and measure the voltage at `soma` and the injection point, to qualitatively replicate Fig. 3.15. To rescale the membrane resistance, use the function `rescale_memb_res` that we provide in the script.

Note: To visually find a compartment to inject current, it is useful to use the point process managers in "Tools -> Point Processes -> Managers" in the NEURON main menu.

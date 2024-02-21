# Bus Clumping Simulation

- Simulation of bus clumping in a bus route ("91") in Milan, Italy using _AnyLogic_. Bus stops loaded onto GIS map with open data, link [here](https://dati.comune.milano.it/dataset/ds534-atm-fermate-linee-di-superficie-urbane).
- Bus clumping is the phenomenon where, in a public transportation route, 2 or more buses/vehicles clump together and move in pairs, instead of ideally having a temporal distance of their interarrival times between each other.
- This can be observed in the real world. This may happen due to numerous reasons but for the scope of this project, the only source of randomness is modelled to be the generationn logic of passengers at the stops, their destinations,
  which will affect the dynamics of the system like the speed of the buses and the service time at the bus stops.
- The aim of this project was to test a conjecture, which is an observation from the real world. The conjecture is, \[within a clumped pair of buses\], the leading bus, on average, tends to have significantly more passengers than the trailing bus.
- The model detects when it encounters bus clumping. It then writes certain parameters of the model onto a .csv file. The most important ones being: number of passengers in the leaading bus and the ones in the trailing one.
- The conjecture was supported by the simulation results, by running the model several times, enough data was generated to analyse a random variable `X`, defined as:
  `X = numOfPass(leadingBus) - numOfPass(trailingBus)`. The distribution of `X` and its expected value support the conjecture.


# The Model

![image](https://github.com/sumdher/BusClumpingAnyLogic/assets/26754139/2bff0a88-64c0-467d-98eb-4903b00f5887)

- The numbers next to the stops in black are the number of passengers waiting at the bus stop.
- The numbers next to the buses in red are the number of passengers inside the bus.

# Some Histograms

<p align="center">
  <img src="https://github.com/sumdher/BusClumpingAnyLogic/assets/26754139/49c07655-321a-40e1-86bf-5b2943b7e680" alt="imgFiltTrailBus" style="width: 45%;"/>
  <img src="https://github.com/sumdher/BusClumpingAnyLogic/assets/26754139/d74cce6d-1d63-4668-aab8-ddca2723aed0" alt="imgLeadBusSize" style="width: 45%;"/>
</p>

It can readily be seen that the leaading buses tend to have more passengers and the trailing buses tend to have fewer passengers.

# Distribution of **X**

![imgNoEqual](https://github.com/sumdher/BusClumpingAnyLogic/assets/26754139/4ec28108-2138-4289-9021-c0823887ca03)
![image](https://github.com/sumdher/BusClumpingAnyLogic/assets/26754139/c5172075-3e69-4084-920f-f60b41eb4787)

## Interpretation:
- The capacity of the buses is 90 passengers max.
- With an expected value of 46, it means that on average, there are 46 more passengers in the leading bus than the ones in the trailing bus, which supports the conjecture.



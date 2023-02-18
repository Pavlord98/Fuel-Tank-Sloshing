# Fuel-Tank-Sloshing

This set of simulations focuses on water sloshing in a tank with and withour baffles. This project is based on and inspired by [this paper](https://www.researchgate.net/publication/286940327_Design_of_fuel_tank_baffles_to_reduce_kinetic_energy_produced_by_fuel_sloshing_and_to_enhance_the_product_life_cycle).

## Pre-analysis

I used the geometry, displacement, and initial water level parameters as seen in the aforementioned paper. 


  
|        Parameter        |                              Value                             |
|:-----------------------:|:--------------------------------------------------------------:|
|        Time step        | starts at 5e-4 but is  adjusted according to  Courant Numbers  |
| Duration of  Simulation |                 At first 1 sec, maybe more soon                |
|  Displacement of  mesh  |                 -15.5[cm]sin((6*pi*t)/(1[s]))cm                |
|     Turbulence model    |                           K Omega SST                          |
|     Height of Water     |                             6.5 cm                             |

## Geometry and Mesh


  

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

I made the geometry in SolidWorks in accordance to the drawings from the paper, and then labeled the patches in Blender in order to prepare the geometry for meshing. 

Here you can see a render of the geometry with the baffles added:

![untitled](https://user-images.githubusercontent.com/84512701/219875106-a873c240-d7b7-46d2-a300-82da9a2ed9f6.png)


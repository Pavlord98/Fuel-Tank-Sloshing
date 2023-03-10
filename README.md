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

I did the meshing with the snappyHexMesh tool with simple parameters and a additional refinement to the cells in the aproximate height of the ininital water level.

![Screenshot 2023-02-18 164817](https://user-images.githubusercontent.com/84512701/219875287-8b1a3845-01a2-4016-82ae-b117362686b9.png)

## Numerical Model

For this simulation I used interFoam, which is a transient, incompressible, turbulent, immisible, isothermal, VOF solver.

For the turbulence model I used the K Omega SST model and initialized the their values using these [recommendations](https://turbmodels.larc.nasa.gov/sst.html).

## Results and postprocessing

![results](https://user-images.githubusercontent.com/84512701/219876698-d09b46eb-80fc-465a-8443-ac42bc3989b6.png)

I expected to see an obvious reduction of sloshing with the added baffles, but based on visual results this isn't very clear. Additional simulations are needed with porous baffles and I plan on doing that soon. Other than that, I should also try the simulations with larger or quicker displacements. 

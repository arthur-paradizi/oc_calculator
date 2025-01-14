# GTNH Batch Size Calculator

## Overview  
The **GTNH Batch Size Calculator** is a Python script designed to calculate optimal batch sizes and overclocking performance for Gregtech machines, currently it includes extra code to support EBF/Volcanus custom heat calculations as well, it generates a graph that plots items per second processed in relation to batch size of the craft, it also outputs to console what the ideal batch size would be when using batch mode.
## How to Use  
Edit the variables listed below and just run the script

---

## Variables to Modify  
The following global variables in the script need to be adjusted based on your specific setup:  

| Variable            | Description                                                                                                                                                     | Default Value |  
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|  
| `IS_EBF`            | Set to `True` if using an Electric Blast Furnace (EBF), otherwise `False`.                                                                                     | `True`        |  
| `MACHINE_POWER`     | The total power available to the machine in EU/t.                                                                                                               | `2048`        |  
| `RECIPE_TIME`       | Base time (in seconds) to complete one recipe.                                                                                                                  | `60`          |  
| `ENERGY_COST`       | Energy cost (in EU) to complete one recipe.                                                                                                                     | `480`         |  
| `ENERGY_DISCOUNT`   | Multiblock-specific energy discount factor.                                                                                                                     | `0.9`         |  
| `SPEED_BOOST`       | Speed boost percentage from multiblock components.                                                                                                             | `120`         |  
| `MAX_PARALLELS`     | Maximum parallel processing slots available for the multiblock.                                                                                                 | `8`           |  
| `COIL_HEAT`         | Heat capacity of the current coil setup (for EBF-specific calculations).                                                                                        | `9901`        |  
| `RECIPE_HEAT`       | Minimum heat required for the recipe (used for EBF-specific calculations).                                                                                      | `2054`        |  


---

## Dependencies  
The script requires the following Python packages:  
- `matplotlib`: For plotting the graph. 

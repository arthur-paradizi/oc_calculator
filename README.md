# GTNH Batch Size Calculator

## Overview  
The **GTNH Batch Size Calculator** is a Python script designed to calculate optimal batch sizes and overclocking performance for a GregTech New Horizons (GTNH) industrial setup. It provides insights into item throughput based on specific machine and recipe parameters and visualizes the performance via a graph.

## Features  
- **Batch Throughput Calculation**: Calculates items processed per second for varying batch sizes.  
- **Overclocking Analysis**: Considers overclocking constraints and recipe-specific parameters.  
- **Visualization**: Generates a graph showing performance trends for batch sizes.  

## How to Use  
The script is executed as a standalone program. It calculates throughput based on customizable variables and generates a graph displaying the results.  

### Key Script Functions  
1. `oc_calculator(batch_size)`  
   - Calculates items per second based on the given batch size and system parameters.  
2. `oc_graph()`  
   - Plots a graph showing items per second for batch sizes ranging from 1 to 10.  

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

Modify these variables in the script to match your machine setup, recipe parameters, and environment.  

---

## Dependencies  
The script requires the following Python packages:  
- `matplotlib`: For plotting the graph.  
- `math`: For performing mathematical calculations.  

### Installing Dependencies  
Run the following command to install the necessary packages:  
```bash
pip install matplotlib


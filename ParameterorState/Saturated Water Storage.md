
parameter_name: sat_deficit

aliases: sat_deficit, sat_deficit_z, water_table_depth

status: complete  
Target ESM: RHESSys, https://github.com/RHESSys/RHESSys.git, develop branch

tags: [parameter, state, hydrology]

Dynamically computed: Yes  
parameter_classification: [geology physical, climate]  
parameter_time_scale: day  
parameter_space_scale: m  
parameter_realism: measurable  
parameter_units: m  
parameter_function: store

# Description  
Represents the vertical distance between the current water table and the soil surface. It quantifies the saturation deficit in the soil profile. Saturation deficit can be translated into depth to water table by integrating over a porosity profile. 

Spatial gradients in saturation deficit (or depth to the water table) are commonly used in hydrologic models to define lateral saturated flow [[Qsat]] magnitude and direction


# Range  
0 to 10s of meters depending on climate, geology and topography

# Function in the model  
Used to compute saturated zone extent and runoff production via saturation excess. Influences capillary rise and water availability to deep roots. Drives the partitioning between saturated and unsaturated flow.

# Sources  


- Databases: Soil and groundwater observations from hydrologic monitoring networks  

# Conceptual or where available mathematical model of parameter variation or controls on the parameter  (for physical parameters only)  

## spatial patterns of saturation deficit/water table

Fan, Ying, H. Li, and Gonzalo Miguez-Macho. "Global patterns of groundwater table depth." _Science_ 339, no. 6122 (2013): 940-943.
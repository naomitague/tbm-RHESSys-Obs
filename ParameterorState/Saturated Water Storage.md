
pparameter_name: sat_deficit

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
Represents the vertical distance between the current water table and the soil surface. It quantifies the saturation deficit in the soil profile and is critical for determining the presence of saturation excess runoff.

# Range  
Typically 0 to several meters, depending on topography, soil properties, and climate.

# Function in the model  
Used to compute saturated zone extent and runoff production via saturation excess. Influences capillary rise and water availability to deep roots. Drives the partitioning between saturated and unsaturated flow.

# Sources  
- Databases: Soil and groundwater observations from hydrologic monitoring networks  
- References on measuring/observing: Penna et al. (2011), "Instrumentation of a catchment for ecohydrological research"  
- From Model Calibration Database: RHESSys calibration datasets  
- From Model Calibration Papers: Tague & Band (2004). "RHESSys: Regional Hydro‑Ecologic Simulation System—An object‑oriented approach to spatially distributed modeling of carbon, water, and nutrient cycling." *Hydrological Processes*, 18(6), 1137‑1157.

# Conceptual or where available mathematical model of parameter variation or controls on the parameter  (for physical parameters only)  
Sat_deficit varies spatially with topographic convergence, soil depth, and land use. Temporally, it is driven by precipitation and evapotranspiration patterns.  
Reference: Tromp‑van Meerveld & McDonnell (2006). Threshold relations in subsurface stormflow: 2. The fill and spill hypothesis. *Water Resources Research*, 42(2).

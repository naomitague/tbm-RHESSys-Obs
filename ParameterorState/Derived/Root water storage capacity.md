
parameter_name: $S_rmax$

aliases: $S_Q$

status: todo
Target ESM: RHESSys, https://github.com/RHESSys/RHESSys.git, develop branch 

tags: [parameter]
# If used to create other parameters, list here

[[Soil Moisture - Root Accessible]]
# Dynamically computed:  
Yes/No
# Select one or more from: geology physical,  geochemical, plant, landuse, snow, climate
parameter_classification []

# Select one: hour, day, month, year, NA
parameter_time_scale: 

# Select one: mm, m, km, plant,NA
parameter_space_scale: 

# Select one: abstract, physical not measurable, measurable
parameter_realism: measurable

# Specify units (e.g., mm/day, gC/m², dimensionless, percent)
parameter_units: m, m^3

# Select one: rate, capacity, ratio, count, store,other
parameter_function: capacity




# Description

Volume or depth of water that can be stored that is accessible by roots. This will depend on both the distribution of roots and physical properties of the soil [[Soil Hydraulic Parameters]] as well as sapprolite and fractured bedrock

# Range

0 - 1500mm 
Stocker, Benjamin D., Shersingh Joseph Tumber-Dávila, Alexandra G. Konings, Martha C. Anderson, Christopher Hain, and Robert B. Jackson. "Global patterns of water storage in the rooting zones of vegetation." _Nature geoscience_ 16, no. 3 (2023): 250-256.




# Function in the model

influences [[Soil Moisture - Root Accessible]]


# Sources
	# Databases
	# References on measuring/observing
	 # From Model Calibration Database
	 # From Model Calibration Papers

# Conceptual or where available mathematical model of parameter variation or controls on the parameter  (for physical parameters only)
	# Summary
	 # References


Sr_max - depends on climate, vegetation and soils.


Stocker, Benjamin D., Shersingh Joseph Tumber-Dávila, Alexandra G. Konings, Martha C. Anderson, Christopher Hain, and Robert B. Jackson. "Global patterns of water storage in the rooting zones of vegetation." _Nature geoscience_ 16, no. 3 (2023): 250-256.


Direct measurement is challenging - 

Small scale - limited from geophysical imaging - which cannot directly measure roots but can infer from water use dynamics

Loiseau, Bertille, Simon D. Carrière, Damien Jougnot, Kamini Singha, Benjamin Mary, Nicolas Delpierre, Roger Guérin, and Nicolas K. Martin-StPaul. 2023. “The Geophysical Toolbox Applied to Forest Ecosystems–A Review.” Science of the Total Environment, 165503.**


Estimated from climatic water deficit in water balance models using  estimate (often remote sensing of ) P and ET - errors in those estimates and the length of time overwhich measurements are available will influences results

Wang-Erlandsson, L., Bastiaanssen, W. G., Gao, H., Jägermeyr, J., Senay, G. B., Van Dijk, A. I., et al. (2016). Global root zone storage capacity from satellite-based evaporation. Hydrology and Earth System Sciences,
20(4), 1459–1481.

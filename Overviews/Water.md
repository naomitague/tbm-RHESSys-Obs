Target ESM: RHESSys, https://github.com/RHESSys/RHESSys.git, develop branch 

alias: [water, hydro]
alias: [stand, plot, patch]

# Overview topic - Select one or more from: water, carbon, energy, nitrogen,  other
overview_constituent: [water]

# Overview scale - Select one or more from: plant, stand/plot/patch, hillslope, watershed
overview_scale: [plot]
# Conceptual Picture of Processes

![hydro](Figures/patch_hydro.jpg)

# List of Key Processes included




process_transpiration
	[[process_stomatal_conductance]]
	

process_soil_evaporation

process_litter_evaporation

process_canopy_evaporation


# List of Outputs Included

output_transpiration
	[[output_stomatal conductance]]

# List of Inputs Included

[[input_precipitation]]

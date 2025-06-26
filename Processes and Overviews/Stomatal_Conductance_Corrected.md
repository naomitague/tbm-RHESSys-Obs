
Target ESM: RHESSys, https://github.com/RHESSys/RHESSys.git, develop branch 

# Tags
process

# Conceptual model
Stomatal conductance (gₛ) is modeled in RHESSys using a Jarvis-type multiplicative approach. Stomatal conductance regulates water and carbon exchange between the leaf and atmosphere and is scaled from a maximum value (gs_max) based on environmental modifiers for light (PPFD), vapor pressure deficit (VPD), air temperature, CO₂ concentration, and root access to water via leaf water potential.

# Model Name (as implemented in the target ESM if there is a standard name e.g Penman monteith)
Jarvis multiplicative stomatal conductance model (after Jarvis 1976, via BIOME-BGC formulation)

# Equation as used in target ESM
gₛ = gₛ_max × f(PAR) × f(CO₂) × f(VPD) × f(Ψ_leaf) x f(t_avg) x f(t_min) * LAI * stomtal_fraction

Where:
- gₛ_max: maximum stomatal conductance (vegetation-specific)
- f(PAR): function of photosynthetically active radiation
- f(CO₂): scalar for CO₂ effect 
- f(VPD): vapor pressure deficit modifier
- [[stomatal_conductance_LWP|f(LWP)]]: function of leaf water potential (soil-moisture mediated)
- f(t_avg) function of daily average air temperature
- f(t_min) function of minimum daily air temperature
- LAI - leaf area index
- stomatal_fraction - density of stomates on the leaf

# Literature References
## References for model in Target ESM
- Running, S.W., & Coughlan, J.C. (1988). A general model of forest ecosystem processes for regional applications: BIOME-BGC.
- Jarvis, P.G. (1976). The interpretation of the variations in leaf water potential and stomatal conductance.

## Alternative Model References

- Damour, Gaëlle, Thierry Simonneau, Hervé Cochard, and Laurent Urban (2010). "An overview of models of stomatal conductance at the leaf level." _Plant, cell & environment_ 33, no. 9 (2010): 1419-1438.-
- - Medlyn, B. E., Duursma, R. A., Eamus, D., Ellsworth, D. S., Prentice, I. C., Barton, C. V. M., et al. (2011). Reconciling the optimal and empirical approaches to modelling stomatal conductance. Global Change Biology, 17(6), 2134–2144. https://doi.org/10.1111/j.1365-2486.2010.02375.x

# Limitations of process implementation used in target ESM
- Assumes one-to-one immediate stomatal response; does not capture dynamic stomatal lag or hysteresis.
- CO₂ response is  non-functional 
- Leaf-level conductance is simplified into sun/shade averages, reducing within-canopy variation.
- No nutrient control on gs, 
- Multiplicative model less mechanistic  - e.g it captures closure due to light availability but this happens because plants don't benefit from water loss in low light - so using A is more coupled - but it is then circular
- No climate acclimation of sensitivity to drivers (e.g t_avg)

# Observations
	# techniques
	 # datasets
	 # patterns 
# Details of  from target ESM model code
##  Variables


	
### fluxes
- stratum_conductance (gs_sunlit, gs_shade)




## parameters (name )
- gs_max
- stomatal_fraction
- Multiplier parameters (all epc structure)
	- vpd  vpd_close, vpd_open
	- psi - psi_close, psi_open (LWP_min_spring), LWP_threshold, LWP_slp, LWP_intercpt
	- tavg - topt, tcoef
- co2_scalar (stubbed or unity)
- epc.ppfd_coef

## Code source file and function names in which process is updated
- `canopy_stratum_daily_F.c`: within `update_vapor_pressure_deficit` and conductance modifiers.

## Code source file in which updated variables are used directly (limit to 4 if used in multiple places)
- penman_monteith.c`: uses stomatal conductance in latent heat flux calculation.
-

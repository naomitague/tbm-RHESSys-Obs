
Target ESM: RHESSys, https://github.com/RHESSys/RHESSys.git, develop branch 

# Tags
process

# Conceptual model
Stomatal conductance (gₛ) is modeled in RHESSys using a Jarvis-type multiplicative approach. It regulates water and carbon exchange between the leaf and atmosphere and is scaled from a maximum value (gs_max) based on environmental modifiers for light (PPFD), vapor pressure deficit (VPD), CO₂ concentration, and water availability via leaf water 
# Model Name (as implemented in the target ESM if there is a standard name e.g Penman monteith)
Jarvis multiplicative stomatal conductance model (after Jarvis 1976, via BIOME-BGC formulation)

# Equation as used in target ESM
gₛ = gₛ_max × f(PAR) × f(CO₂) × f(VPD) × f(Ψ_leaf)

Where:
- gₛ_max: maximum stomatal conductance (vegetation-specific)
- f(PAR): function of photosynthetically active radiation
- f(CO₂): scalar for CO₂ effect (often unity in current RHESSys)
- f(VPD): vapor pressure deficit modifier
- f(Ψ_leaf): function of leaf water potential (soil-moisture mediated)
- f(t_min), f(t_avg) function of daily average and daily minimum temperatures
gs_canopy = gs*LAI * stomatal_fraction

computed separately for sunlit and shaded parts of the canopy
# Literature References
## References for model in Target ESM
- Running, S.W., & Coughlan, J.C. (1988). A general model of forest ecosystem processes for regional applications: BIOME-BGC.
- Tague, C. & Band, L. (2004). RHESSys model framework description.
- Jarvis, P.G. (1976). The interpretation of the variations in leaf water potential and stomatal conductance.

## Alternative Model References
- Ball, J.T., Woodrow, I.E., & Berry, J.A. (1987). Ball–Berry empirical stomatal model.
- Medlyn, B.E. et al. (2011). Optimization-based stomatal conductance model.
- Buckley, T.N., Mott, K.A., & Farquhar, G.D. (2003). BMF process-based stomatal model.

# Limitations of process implementation used in target ESM
- Assumes steady-state response; does not capture dynamic stomatal lag or hysteresis.
- Leaf-level conductance is simplified into sun/shade averages, reducing within-canopy variation.
- No mechanistic hydraulic feedback or assimilation optimization-based closure.

# Details of  from target ESM model code
##  Variables

## Observations
### fluxes
- gs_sunlit
- gs_shaded



### stores
- Leaf water potential (Ψ_leaf)
- Soil water potential (Ψ_soil)

## parameters (name )
- gs_max
- vpd_close
- vpd_open
- psi_close
- psi_open
- co2_scalar (stubbed or unity)
- epc.ppfd_coef

## Code source file and function names in which process is updated
- `canopy_stratum_daily_F.c`: within `update_vapor_pressure_deficit` and conductance modifiers.
- `compute_transmissivity_curve.c`: modifies light inputs for sunlit/shaded LAI.
- `compute_penman_monteith.c`: uses stomatal conductance in latent heat flux calculation.

## Code source file in which updated variables are used directly (limit to 4 if used in multiple places)
- `compute_penman_monteith.c`
- `compute_subsurface_routing_topmodel.c` (indirectly via water balance)
- `photosynthesis.c` (carbon gain feedback)
- `surface_energy_balance.c`

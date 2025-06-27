# Parameter Name
psi_threshold, psi_wilt

# Description
Threshold and wilting point values (in MPa) used to compute the stomatal conductance response to leaf water potential.

# Units
MPa

# Range
Typical range for psi_threshold: -0.5 to -1.5  
Typical range for psi_wilt: -1.5 to -4.0

# Function in Model
Modulates the multiplier applied to potential stomatal conductance based on current leaf water potential.

# Model
## Summary
Stomatal conductance declines linearly from psi_threshold to psi_wilt, reaching zero below psi_wilt.

## References
- Tague, C.L., & Band, L.E. (2004)
- Sperry et al. (2002), Williams et al. (1996)

# Sources
## Databases
- TRY Plant Trait Database (https://www.try-db.org)
- EcoHydros Database (site-specific field data)

## References
### From Model Calibration Database
Values may be tuned per plant functional type or vegetation stratum

### From Model Calibration Papers
Site-specific values often derived from hydraulic vulnerability curves or inferred from stomatal behavior studies.

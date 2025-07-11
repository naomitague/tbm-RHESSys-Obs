Target ESM: RHESSys, https://github.com/RHESSys/RHESSys.git, develop branch

# constituent
output_constituent: [water]

# kind
output_kind: [flux]

# units
output_units: [mm/day]

# Description
Transpiration represents the flux of water vapor from plant surfaces to the atmosphere, primarily through stomatal openings. It is influenced by meteorological conditions, leaf physiology, and soil water availability. 
Importantly, transpiration is not evaporation - so observations of ET needed to be combined with the partition of water flux between transpiration and evaporation

# Process Links
[[process_transpiration]]

# Measurements

## Techniques, Product Evaluation, Error/Uncertainty Papers
- **Sap flow sensors** for direct measurement of water flux in tree stems:
  - Lu, P., Urban, L., & Zhao, P. (2004). Granier’s thermal dissipation probe (TDP) method for measuring sap flow in trees: theory and practice. _Acta Botanica Sinica_, 46(6), 631–646.

- **Eddy covariance methods** for stand-scale evapotranspiration partitioning:
  - Wilson, K. B., Baldocchi, D. D., & Hanson, P. J. (2001). Leaf area index and light extinction coefficients. _Agricultural and Forest Meteorology_, 107(1), 93–115.

- **Isotope and modeling techniques** to separate transpiration from evaporation:
  - Wang, L., et al. (2014). Partitioning evapotranspiration across gradients of woody plant cover: Comparison of isotopic and micrometeorologic methods. _Agricultural and Forest Meteorology_, 184, 132–142.

- **Remote sensing** using thermal imaging to infer transpiration rates:
  - Fisher, J.B., et al. (2020). The future of evapotranspiration: Global requirements for ecosystem functioning, carbon and climate feedbacks, agricultural management, and water resources. _Water Resources Research_, 56(4), e2019WR026236.
  - Zhang, Ke, John S. Kimball, and Steven W. Running. "A review of remote sensing based actual evapotranspiration estimation." _Wiley interdisciplinary reviews: Water_ 3, no. 6 (2016): 834-853.

## Sources/Database
- FLUXNET https://fluxnet.org/
- SAPFLUXNET global database of sap flow data (DOI |10.5281/zenodo.2530797)
Poyatos, R., Granda, V., Flo, V., Adams, M.A., Adorján, B., Aguadé, D., Aidar, M.P., Allen, S., Alvarado-Barrientos, M.S., Anderson-Teixeira, K.J. and Aparecido, L.M., 2020. Global transpiration data from sap flow measurements: the SAPFLUXNET database. _Earth System Science Data Discussions_, _2020_, pp.1-57

Satellite ET estimates https://www.earthdata.nasa.gov/topics/atmosphere/evapotranspiration/data-access-tools

# Model Output Paper Examples
## References
- Wang, Kaicun, and Robert E. Dickinson. "A review of global terrestrial evapotranspiration: Observation, modeling, climatology, and climatic variability." _Reviews of Geophysics_ 50, no. 2 (2012).
- Kool, D., Agam, N., Lazarovitch, N., Heitman, J.L., Sauer, T.J. and Ben-Gal, A., 2014. A review of approaches for evapotranspiration partitioning. _Agricultural and forest meteorology_, _184_, pp.56-70.

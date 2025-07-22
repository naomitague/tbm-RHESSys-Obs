parameter\_name: K\_s (saturated hydraulic conductivity)

aliases: Ksat, saturated conductivity, Ks

status: todo

Target ESM: RHESSys, https\://github.com/RHESSys/RHESSys.git, develop branch

# If used to create other parameters, list here

[[transmissivity]]

# Select one or more from: geology physical,  geochemical, plant, landuse, snow, climate

parameter\_classification [geology physical]

# Select one: hour, day, month, year, NA

parameter\_time\_scale: NA

# Select one: mm, m, km, plant,NA

parameter\_space\_scale: mm

# Select one: abstract, physical not measurable, measurable

parameter\_realism: measurable

# Specify units (e.g., length/time,  gC/m², dimensionless)

parameter\_units: length/time

# Select one: rate, capacity, ratio, count, other

parameter\_function: rate

tags: [parameter]

# Description

Saturated hydraulic conductivity represents the maximum rate at which water can move through soil when all pores are water-filled. It reflects the ease of water movement through saturated soil and is a primary control on infiltration and subsurface flow.

# Range

Typical values:

- Sands: 1000 to 10,000 mm/day
- Loams: 10 to 100 mm/day
- Clays: 0.01 to 10 mm/day

However most saturated hydraulic conductivity in soils and other substrates is often much higher than expected given texture due to macropores and preferential flowpaths - Many models calibrate or infer and "effective hydraulic conductivity", Or use a two layer approach where water flows through a soil matrix and through macropores.  This coupled with high heteorogenity in soil/substrate means that saturated hydraulic conductivity is often inferred from inverse modeling (or calibration of more complex hydrologic models), Importantly this also means that K_\s is not scale independent, such that average of smaller scales (e.g plot) do not provide correct estimates at larger scales (e.g hillslope/watershed)

# Function in the model

K\_s determines the upper limit of vertical and lateral drainage in saturated or near-saturated conditions. In RHESSys, it influences saturated flow, especially during storm events, recharge, and redistribution phases.

# Sources

```
# Databases
```

# References on measuring observing
 - Field and lab methods include constant/falling head permeameter tests, Guelph permeameter, and tension infiltrometers.
 - Pedotransfer functions estimate K_s based on texture, bulk density, and organic matter content.


# Conceptual model of parameter variation or controls on the parameter  (for physical parameters only)

```
# Summary
```

Controlled primarily by soil texture, structure, compaction, and saturation. Sandy soils with large pores have high K\_s values, while clayey soils with micropores exhibit low values. Macropores and bioturbation can increase K\_s dramatically in aggregated soils.

```
# References
```

See [[Soil Hydraulic Parameters]] for broader context and sources for soil hydraulic parameters.
but also consider references on macropores and preferential flowpaths discuss how to include these in models

Assessing measurement approaches
Sun, Dongwei, Ning Luo, Aaron Vandenhoff, Wesley McCall, Zhanfeng Zhao, Chenxi Wang, David L. Rudolph, and Walter A. Illman. "Evaluation of hydraulic conductivity estimates from various approaches with groundwater flow models." _Groundwater_ 62, no. 3 (2024): 384-404.

Role of macropores
Beven, Keith, and Peter Germann. "Macropores and water flow in soils revisited." _Water resources research_ 49, no. 6 (2013): 3071-3092.


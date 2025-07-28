# Santanello Soil Heat Flux Python Package

This package provides a Python implementation of the soil heat flux (G) calculation based on the method proposed by Santanello and Friedl (2003). The algorithm estimates soil heat flux as a function of time of day, net radiation, and soil moisture, capturing the diurnal cycle and moisture dependence of land surface energy balance.


Gregory H. Halverson (they/them)<br>
[gregory.h.halverson@jpl.nasa.gov](mailto:gregory.h.halverson@jpl.nasa.gov)<br>
NASA Jet Propulsion Laboratory 329G


## Features

- Implements the Santanello & Friedl (2003) soil heat flux (G) calculation using published relationships.
- Accepts both numpy arrays and Raster objects for input data.
- Models diurnal variation and soil moisture dependence of soil heat flux.


## Installation

Install the `santanello-soil-heat-flux` package from PyPi using pip:

```fish
pip install santanello-soil-heat-flux
```


## Usage

Import the main function and use it with your raster or numpy array data:

```python
from santanello_soil_heat_flux import santanello_soil_heat_flux

G = santanello_soil_heat_flux(seconds_of_day, Rn, SM)
```

Where:
- `seconds_of_day`: Time in seconds since midnight
- `Rn`: Net radiation in W/m²
- `SM`: Soil moisture in m³/m³


## References

Santanello, J. A., & Friedl, M. A. (2003). Diurnal covariation in soil heat flux and net radiation. *Journal of Applied Meteorology*, 42(6), 851-862.

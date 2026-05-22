# SAI Overshoot Analysis

Code for the analysis in:

> Egbebiyi et al. (2026). *[Manuscript title]*. Submitted to [Journal name].

This repository contains the Jupyter notebook used to compute climate indices, surface moisture budget, and statistical detectability for the African continent under SSP5-8.5, SSP5-3.4-OS, and stratospheric aerosol injection scenarios using CESM2-WACCM6 output.

## Contents

- `climate_analysis.ipynb` — main analysis notebook covering:
  - ETCCDI climate indices (R1mm, Rx5day, CWD, CDD, SDII, PRCPTOT) via xclim
  - Growing degree days, mean temperature, and optimal growing days
  - Warm spell duration index using the 90th percentile of daily maximum temperature
  - Surface moisture budget (P minus ET) over West, Central, East, and Southern Africa
  - Welch's t-test for grid-cell significance and the detectability heatmap

## Data

The analysis uses CESM2-WACCM6 output from the simulations described in Tilmes et al. (2020). Variables used are TREFHT, TREFHTMX, PRECT, and LHFLX. Data paths in the notebook (`prec_data_dir`, `temp_data_dir`, `tmax_data_dir`, `flux_data_dir`) should be updated to point to local copies of the model output.

## Requirements

Python 3.9+ with the following packages:

```
xarray
numpy
pandas
scipy
matplotlib
cartopy
shapely
xclim
netCDF4
```

Install with:

```bash
pip install -r requirements.txt
```

## Citation

If you use this code, please cite the manuscript above and this repository via its Zenodo DOI:

[Zenodo DOI badge will appear here once minted]

## Contact

Temitope Egbebiyi  
African Climate and Development Initiative, University of Cape Town  
ffrtem001@myuct.ac.za

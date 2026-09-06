# Stomatal behaviour across tree species predicts physiological drought stress but weakly reflects leaf traits

## Project Description

This repository contains the R scripts used to analyse species-specific stomatal behaviour across 38 tree species.

The project investigates how stomatal responses to increasing atmospheric vapour pressure deficit (VPD) vary among tree species and whether these responses are related to functional leaf traits and drought-related physiological stress.


The analyses support the manuscript:

> Sachsenmaier et al. (2026). Stomatal behaviour across 38 tree species shows weak associations to leaf traits but reflect physiological drought stress

---

## Workflow overview

### Rmd Scripts

The following Scripts should be run in numeric order:

01_data_cleaning.Rmd

* imports the raw data set of stomatal conductance
* performs quality control
* prepares the analysis dataset

02_main_model_and_metrics.Rmd

* fits nonlinear Bayesian hierarchical models using brms
* estimates species-specific stomatal response curves
* extracts posterior-derived stomatal behaviour metrics:
  * maximum stomatal conductance (gs max)
  * VPD optimum (VPDopt)
  * VPD at 50 % stomatal closure (VPD50)
  * stomatal closure rate (Sdecline)
  
03_trait_and_drought_stress_analysis.Rmd

* analyses relationships between stomatal behaviour and leaf functional traits
* analyses relationships between stomatal behaviour and leaf carbon isotope discrimination in 2018 compared to 2021

04_environmental_conditions.Rmd

* processes environmental variables from sensors and climate station
* checks the status of soil moisture and VPD across the measurement time


### Data sets

The following data sets are in the raw data folder of this repository:

* data_stomatal_conductance.csv --> main data set of the study, to be found in the raw data folder
* climate_sensor_at_site.csv --> to be found in the raw data folder

These datasets are for now in the raw data folder (so that the Scripts run for the co-authors/reviewers, but will be published on Zenodo soon):
* data_stomata_traits_angio.csv
* data_leaf_morphology.csv
* data_leaf_chemistry.csv
* data_leaf_carbon_isotopes_2018_2021.csv

This data set is already published and can be downloaded from Zenodo:
* Sachsenmaier_et_al_2026_conifer_stomata_trait_data.csv --> "https://zenodo.org/records/21098915/files/Sachsenmaier_et_al_2026_conifer_stomatal_trait_data.csv?download=1"

Climate data can be downloaded from the Climate Data Center (CDC):
* https://opendata.dwd.de/climate_environment/CDC/observations_germany/climate/daily/kl/historical/ 
select the climate station Leipzig/Halle (Station ID: 02932)


### Output

All figures, tables, supplementary figures and tables that are shown in the respective manuscript are produced and stored in the folder "output"



## Requirements

The analyses were performed using:

- R version 4.5.3
- RStudio (recommended)

Package dependencies are managed using [`renv`](https://rstudio.github.io/renv/).

Please see renv.lock file.

## Contributors and Contact

Authors:

Lena Sachsenmaier
Co-authors listed in the associated manuscript

For questions regarding the analysis or code, please contact:

Lena Sachsenmaier
lena.sachsenmaier.research@gmail.com

If you use this repository, please cite the associated publication.


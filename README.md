# Stomatal sensitivity to VPD across 38 tree species reflects past drought responses

## Project Description

This repository contains the R scripts used to analyse species-specific stomatal behaviour across 38 tree species.

The project investigates how stomatal responses to increasing atmospheric vapour pressure deficit (VPD) vary among tree species and whether these responses are related to physiological drought responses and stomatal anatomy & leaf economic traits.


The analyses support the submitted manuscript:

> Sachsenmaier et al. (2026). Stomatal sensitivity to VPD across 38 tree species reflects past drought responses

---

## Workflow overview

### Rmd Scripts

The following R Scripts should be run in numeric order:

00_setup.Rmd

* sets up a folder structure
* downloads all published raw data sets used in this study from Zenodo


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
  
03_analyses_drought_responses_and_leaf_traits.Rmd

* analyses relationships between stomatal behaviour and leaf carbon isotope discrimination in 2018 compared to 2021
* analyses relationships between stomatal behaviour and leaf functional traits

04_environmental_conditions.Rmd

* processes environmental variables from sensors and climate station
* checks the status of soil moisture and VPD across the measurement time


### Data sets

Some data sets are already published on Zenodo and publicly available:
(you don't need to download them separately, is done automated in the Script 00_setup.Rmd)

* stomatal anatomy trait data - angiosperms:

  Kretz, L., Sachsenmaier, L., von Sivers, L., Nabel, N., Wirth, C., & Weigelt, A. (2026). Stomatal density and size of 27 angiosperm tree species (ARBOfun       research arboretum, Germany) (Version 1.0.0) [Dataset]. Zenodo. https://doi.org/10.5281/zenodo.22117766
  
* stomatal anatomy trait data - gymnosperms:

  Sachsenmaier, L., Franz, S., Kahl, A., Kretz, L., & Wirth, C. (2026). Stomatal density and size of 12 conifer tree species (Version 1.0.0) [Dataset]. Zenodo.   https://doi.org/10.5281/zenodo.21098915
  
* leaf functional trait data:

  Kretz, L. et al (2026) - Leaf functional traits
  10.5281/zenodo.21821305
  (DOI not yet working; will fix this)


Other data sets are currently restricted and only made available for peer-review via a private link. Upon publication of the submitted manuscript these data    sets will be also publicly available:


* main dataset of the study:
   * data stomatal conductance
   * associated climate station data of the site
 

* leaf carbon isotope data:

Kahl, A., Schnabel, F., Richter, R., Olbrich, J., Zahner, G., Weigelt, A., & Wirth, C. (2026). Leaf δ¹³C of 38 tree species measured in 2018 and 2021 (ARBOfun research arboretum, Germany) [Dataset]. Zenodo. https://doi.org/10.5281/zenodo.22284412


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


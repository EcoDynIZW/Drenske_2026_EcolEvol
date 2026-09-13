# Decoupled genetic and demographic responses to urbanization in a small mammal population
 
Sinah Drenske, Conny Landgraf, Alina Theresa Berger, Alina Doreen Stemmer, Aimara Planillo, Johanna Leona Eul, Bianca Wist, Kathleen Röllig, Ashlee Jean Mikkelsen, Melanie Dammhahn, Jörns Fickel, Stephanie Kramer-Schadt

DOI: 10.1002/ece3.74273
  
## Abstract

Urbanization influences ecological and evolutionary processes, including gene flow and survival. Understanding how genetic and demographic rates respond to urbanization is therefore essential for wildlife viability in human-dominated landscapes. We tested whether population genetic diversity, genetic structure, and apparent survival of Eurasian red squirrels (*Sciurus vulgaris*) vary in concert along an urbanization gradient. We combined a multi-year capture–mark–recapture study with microsatellite-based population genetic analyses at three sites in Berlin, Germany, representing increasing levels of urbanization. Genetic diversity was broadly comparable among sites, indicating no strong genetic erosion in urban populations. However, weak heterozygote deficits and subtle differences in individual heterozygosity suggest mild restrictions to gene flow along the urban gradient. Bayesian clustering analyses identified two genetic clusters, broadly corresponding to study sites, revealing emerging fine-scale population structure despite the small spatial extent of the study area. Apparent survival did not differ clearly among sites. Several predictors received similar support, highlighting substantial uncertainty in the drivers of survival in this system. By integrating genetic and demographic data, our study demonstrated that fine-scale genetic structuring can emerge in urban wildlife populations without translating into detectable short-term differences in apparent survival. These findings highlight that genetic and demographic responses to urbanization can be decoupled and emphasize the importance of integrated approaches for understanding population survival in human-modified environments.

## Description of the data and file structure
 
 - data-raw: Contains the raw datasets used in this project, including capture–mark–recapture data, genetic data, and spatial data used for mapping.
 - output: Contains processed datasets generated during the analysis.
 - plots: Contains figures generated during data exploration and analysis.
 - R: Contains all R scripts used for data processing, analysis, and figure generation.

## Data description
- Capture-mark-recapture data: Capture histories and associated metadata used for survival analyses.
- Genetic data: Microsatellite genotype data used for population genetic analyses + STRUCTURE results.
- Spatial data: Geographic data used to generate maps of the study area and sampling locations.

## Description of the R files

*01_identity_analysis*: Combines identity analysis results from Cervus with capture-mark-recapture data to assess whether genotypes may belong to the same individual and to compare attributes such as study site and sex.

*02a_squirrel_cmr_data_preparation*: Preparation of datasets for CMR analysis, trapping effort, and human activity variables (e.g., adding or transforming columns).

*02b_squirrel_cmr_data_exploration*: Exploratory analyses of the datasets using summary tables and plots.

*02c_squirrel_cmr_trap_locations*: Creation of maps of the overall study area (Berlin) and the individual study sites. 

*03_genetics_kinship_coefficient*: Kinship analysis using the R package related. The Queller & Goodnight kinship coefficient was calculated and closely related individuals were subsequently removed from the dataset afterwards.

*04_genetics_description_populations*: Calculation of population genetic metrics describing the study populations and the overall dataset, including allelic richness, private alleles, effective number of alleles, and observed and expected heterozygosity.

*05_genetics_population_differences*: Estimation of metrics describing population differentiation, including pairwise FST values.

*06a_genetics_cluster_analysis_data_preparation*: Preparation of STRUCTURE outputs for downstream analysis.

*06b_genetics_cluster_analysis_evanno_method_comparison*: Cluster analysis using the Evanno method to determine the most likely number of genetic clusters based on STRUCTURE simulation results.

*07a_survival_preparation*: Preparation of datasets for survival analyses, including generation of individual capture histories and addition of time-varying covariates.

*07b_survival_analysis*: Estimation of apparent survival using the package RMark and model selection.

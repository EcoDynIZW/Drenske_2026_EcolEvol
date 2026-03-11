# Decoupled genetic and demographic responses to urbanization in a small mammal population
 
Sinah Drenske, Conny Landgraf, Alina Theresa Berger, Alina Doreen Stemmer, Aimara Planillo, Johanna Leona Eul, Bianca Wist, Kathleen Röllig, Ashlee Jean Mikkelsen, Melanie Dammhahn, Jörns Fickel, Stephanie Kramer-Schadt

DOI: TBA
  
## Abstract

1.	Urbanization influences ecological and evolutionary processes, including gene flow and survival. Understanding how genetic and demographic rates respond to urbanization is there-fore essential for wildlife viability in human-dominated landscapes. We tested whether pop-ulation genetic diversity, genetic structure, and apparent survival of Eurasian red squirrels (Sciurus vulgaris) vary in concert along an urbanization gradient.
2.	We combined a multi-year capture–mark–recapture study with microsatellite-based popula-tion genetic analyses at three sites in Berlin, Germany, representing increasing levels of ur-banization. 
3.	Genetic diversity was broadly comparable among sites, indicating no strong genetic erosion in urban populations. However, weak heterozygote deficits and subtle differences in indi-vidual heterozygosity suggest mild restrictions to gene flow along the urban gradient. Bayesi-an clustering analyses identified two genetic clusters, broadly corresponding to study sites, revealing emerging fine-scale population structure despite the small spatial extent of the study area.
4.	Apparent survival did not differ clearly among sites. Several predictors received similar sup-port, highlighting substantial uncertainty in the drivers of survival in this system.  
5.	By integrating genetic and demographic data, our study demonstrated that fine-scale genetic structuring can emerge in urban wildlife populations without translating into detectable short-term differences in apparent survival. These findings highlight that genetic and demographic responses to urbanization can be decoupled and emphasize the importance of integrated ap-proaches for understanding population survival in human-modified environments.

## Description of the data and file structure
 
 - data-raw: This folder stores the raw data used in this project (Divided in capture-mark-recapture data, geentics and geodata used for maps)
 - output: here you can find the processed data used for the analysis
 - plots: This folder contains plots used for the analysis
 - R: Contains the R scripts for the project

## Description of the R files

*01_identity_analysis*: After identity analysis with Cervus: Could the indiviuals be the same? Do they stem e.g. from the same study site, same sex etc. Here we combine the results from Cervus with our cmr-data to compare.

*02a_squirrel_cmr_data_preparation*: Prepapration of the datasets for CMR, trapping effort and human activity. E.g. adding new columns, 

*02b_squirrel_cmr_data_exploration*: Explore the datasets in different ways with a lot of plots and tables

*02c_squirrel_cmr_trap_locations*: Create maps of the whole study area (Berlin) and the single study sites 

*03_genetics_kinship_coefficient*: Kinship analysis with the package r-reltaed. We calculated the Queller & Goodnigth kniship coefficient and afterwards we removed closely related individuals from the raw dataset.

*04_genetics_description_populations*: We calculated different population genetic metrics to describe the populations on our study sites and in total. We calculated for example Allelic richness, Private alleles, Effective number of alleles, observed and expeted heterozygosity etc. 

*05_genetics_population_differences*: We claculated metrics to analyse population differences like pairwise FST values

*06a_genetics_cluster_analysis_data_preparation*: Preparation of the Results of the STRUCTURE analysis for further anaylsis

*06b_genetics_cluster_analysis_evanno_method_comparison*: We conducted the Cluster anaylsis with the Evanno method with the Results from STRUCTRE simulations.

*07a_survival_preparation*: Preparation of the data for the survival analysis e.g. preparing the individual capture histories and adding time-varying covariates.

*07b_survival_analysis*: Survival analysis with RMark

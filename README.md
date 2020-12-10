#TFCB Capstone Project
 This document describes Cassidy Danyko's 2020 TFCB Capstone Project

 
## Data and Citation
Data downloaded from:[Glaucoma diagnosis](https://datadryad.org/stash/dataset/doi:10.5061/dryad.q6ft5)
Kim, S. J., Cho, K. J. & Oh, S. Development of machine learning models for diagnosis of glaucoma. PLoS ONE 12, e0177726 (2017).

This includes three csv files:
- ds_test
	- Columns include RL; glaucoma; age; ocular_Pressure; MD; PSD; GHT; cornea_thickness; RNFL4.mean
- ds_train
- ds_whole

##Project Organization
 two report R fies
 jupyter notebook
 
##About the Analysis 
###Question 1
 What are the max and min ratios of ocular_pressure to cornea thickness for those with glaucoma
 Use tidyverse in R
 read test csv file
 glaucoma = 1 
 make ratio column
 sort by that column
 get max and min
 
 
### Question 2
 Plot the relationship between age and RNFL4.mean
 Use ggplot in R
 
### Question 3
 python jupyter notebook with ggplot
 
 

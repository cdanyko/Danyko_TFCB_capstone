# Cassidy Danykos TFCB Capstone Project

## Data and Citation
Data downloaded from:[Glaucoma diagnosis](https://datadryad.org/stash/dataset/doi:10.5061/dryad.q6ft5)

Kim, Seongjae; Cho, Kyung Jin; Oh, Sejong (2018), Data from: Development of machine learning models for diagnosis of glaucoma, Dryad, Dataset, https://doi.org/10.5061/dryad.q6ft5


### This includes three csv files:
- ds_test
- ds_train
- ds_whole
Columns:    
RL | glaucoma | age | ocular_Pressure | MD | PSD | GHT | cornea_thickness | RNFL4.mean


### Assumptions on data 
RNFL: retinal nerve fiber layer thickness  
VF: visual field  
MD: mean VF distance  
PSD:pattern standard deviation (progression of glaucoma)  
OD:right eye  
OS: left eye  

 
## About the Analyses 
- I used R Markdown, Markdown, and Python in this project.
	- In R Markdown, load tidyverse, dplyr, scales, ggplot2)
	- In Jupyter Notebook, import matplotlib.pyplot as plt; import pandas as pd; from sklearn.decomposition import PCA; from sklearn.preprocessing import StandardScaler
- I used ds_whole for all analyses.  This file contains the data from both ds_test and ds_train.

### Question 1: How many entires are predicted to have glaucoma (glaucoma = 1) ? What is the max RNFL4.mean of those predicted to have glaucoma. Compare to mean of those predicted not to have glaucoma? Is the value of  RNFL4.mean able to predict glaucoma ?
- This was completed in file [Capstone.rmd)](Capstone.rmd) 
- Read csv file, filter for glaucoma=0 or glaucoma=1, get max and mins, use arithmetic to compare.

 

### Question 2: How does the ratio between ocular_pressure and cornea thickness change with age.
- This was completed in file [Capstone.rmd)](Capstone.rmd) 
- mutate to create a new column of the ratio, select these columns and use ggplot to make a geo_point graph. I used a binned scale to better represent the data by age group.
 
 
### Question 3: Do these data show nice grouping in PCA analysis between MD and RNFL4.mean?
- This was completed in file [Capstone_JN.ipynb](Capstone_JN.ipynb)
- load data into dataframe, remove RL and glaucoma columns, PCA and plot. 
 
## Reproducibility
The data available for this study had no readme file to explain the data.
They did not provide a key to understanding the data, including but not limited to information about the column names and analysis done on the data. 
They also did not provide code to process this data.
These data do not follow reproducibility guidelines because I cannot take the raw data  and run the same analysis that the author used and confirm that it generates the same results. 

The analyses I've completed have reproducibility notes in each document. I have followed reproducibility guidelines by including the datafiles and analyses within a single git hub project. 
 
 

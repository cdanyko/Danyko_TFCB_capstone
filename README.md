#TFCB Capstone Project
 This document describes Cassidy Danyko's 2020 TFCB Capstone Project

 
## Data and Citation
Data downloaded from:[Glaucoma diagnosis](https://datadryad.org/stash/dataset/doi:10.5061/dryad.q6ft5)
Kim, Seongjae; Cho, Kyung Jin; Oh, Sejong (2018), Data from: Development of machine learning models for diagnosis of glaucoma, Dryad, Dataset, https://doi.org/10.5061/dryad.q6ft5

### Abstract: The study aimed to develop machine learning models that have strong prediction power and interpretability for diagnosis of glaucoma based on retinal nerve fiber layer (RNFL) thickness and visual field (VF). We collected various candidate features from the examination of retinal nerve fiber layer (RNFL) thickness and visual field (VF). We also developed synthesized features from original features. We then selected the best features proper for classification (diagnosis) through feature evaluation. We used 100 cases of data as a test dataset and 399 cases of data as a training and validation dataset. To develop the glaucoma prediction model, we considered four machine learning algorithms: C5.0, random forest (RF), support vector machine (SVM), and k-nearest neighbor (KNN). We repeatedly composed a learning model using the training dataset and evaluated it by using the validation dataset. Finally, we got the best learning model that produces the highest validation accuracy. We analyzed quality of the models using several measures. The random forest model shows best performance and C5.0, SVM, and KNN models show similar accuracy. In the random forest model, the classification accuracy is 0.98, sensitivity is 0.983, specificity is 0.975, and AUC is 0.979. The developed prediction models show high accuracy, sensitivity, specificity, and AUC in classifying among glaucoma and healthy eyes. It will be used for predicting glaucoma against unknown examination records. Clinicians may reference the prediction results and be able to make better decisions. We may combine multiple learning models to increase prediction accuracy. The C5.0 model includes decision rules for prediction. It can be used to explain the reasons for specific predictions.

###This includes three csv files:
- ds_test
	- Columns include 
	RL|glaucoma|age|ocular_Pressure|MD|PSD|GHT|cornea_thickness|RNFL4.mean
- ds_train
- ds_whole

###Assumptions on data 
RNFL: retinal nerve fiber layer thickness and
VF: visual field
MD: mean VF distance
PSD:pattern standard deviation (progression of glaucoma)
OD:right eye
OS: left eye

 
##About the Analyses 
-I used R Markdown, Markdown, and Python in this project.
-In R Markdown, load tidyverse, dplyr, scales, ggplot2)
-In Jupyter Notebook, import matplotlib.pyplot as plt; import pandas as pd; from sklearn.decomposition import PCA; from sklearn.preprocessing import StandardScaler
-I used ds_whole for all analyses.  This file contains the data from both ds_test and ds_train.

###Question 1: How many entires are predicted to have glaucoma (glaucoma = 1) ? What is the max RNFL4.mean of those predicted to have glaucoma. Compare to mean of those predicted not to have glaucoma? Is the value of  RNFL4.mean able to predict glaucoma ?
- This was completed in file [Capstone.rmd)](Capstone.rmd) 
- Read csv file, filter for glaucoma=0 or glaucoma=1, get max and mins, use arithmetic to compare.

 

###Question 2: #How does the ratio between ocular_pressure and cornea thickness change with age.
- This was completed in file [Capstone.rmd)](Capstone.rmd) 
- mutate to create a new column of the ratio, select these columns and use ggplot to make a geo_point graph. I used a binned scale to better represent the data by age group.
 
 
### Question 3
Do these data show nice grouping in PCA analysis between MD and RNFL4.mean?
- This was completed in file [Capstone_JN.ipynb](Capstone_JN.ipynb)
- load data into dataframe, remove RL and glaucoma columns, PCA and plot. 
 
##Reproducibility
The data available for this study had no readme file to explain the data.
They did not provide a key to understanding the data, including but not limited to information about the column names and analysis done on the data. 
They also did not provide code to process this data.
These data do not follow reproducibility guidelines because I cannot take the raw data  and run the same analysis that the author used and confirm that it generates the same results. 

The analyses I've completed have reproducibility notes in each document. I have followed reproducibility guidelines by including the datafiles and analyses within a single git hub project. 
 
 

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
 
 ###
### Create a summary chart of the average RLRNFL4.mean for both eyes(group OD OS with index below meh )
 Plot the relationship between age and RNFL4.mean
 Use ggplot in R
 
### Question 3
 python jupyter notebook with ggplot
 
##Reproducibility
 
 

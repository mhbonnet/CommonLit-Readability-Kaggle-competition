# Kaggle8 repository - CommonLit Readability Kaggle competition
  
This repository contains different notebooks created for the Kaggle competition : 'CommonLit Readability'.   

For this competition, I tried two different approaches using DistilBert.   
  
In the first approach, I used Distilbert as a feature extractor, and the features were then given to regressors. Two notebooks concerns this approach :   
* In **'Full compare Projet 8'** notebook, you'll find a comparison between different regression models applied on the same features, extracted with the pretrained DistilBert model.   
* The **'distilbert-for-regression'** notebook contains the first code submitted for the competition : features extracted with the DistilBert pretrained model and a ridge regression with a polynomial kernel (best RMSE = 0.561).    

In the second approach I build a composed pytorch model with Distilbert, dropout and linear layers. The code was originally copied from other notebooks (S Canisir et V Baskaran). I upgraded it in two steps, resulting is the two notebooks below, both submitted to the competition (best RMSE = 0.576).  
* **'commonlit-distilbert-all-in-one'** : RMSE and learning curves display 
* **'distilbert-fine-tuning-data-augmentation'** : data augmentation

All of these notebooks require the import af a distilbert-base-uncased dataset in Kaggle, in order to use pretrained model offline. The last notebook requires also the import of a nlpaug dataset to be used offline.
    
The 'requirements.txt' file contains all the librairies available in the Kaggle envrionment for the submission to the competition.
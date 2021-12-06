# Spatial-attention and Demographic-augmented Generative Adversarial Imputation Network

## Update: Experimental results in rebuttal
1. About data missing rates and missing patterns

The experimental results at low missing rates (25% missing) are shown below. From the results we can see that the advantage of SDA-GAIN is reduced but still as good as other baseline methods.
<img src="https://github.com/WoodScene/Paper_pictures/blob/main/KDD2021/UK_RMSE.png" width="400" height="360"/><br/>
<img src="https://github.com/WoodScene/Paper_pictures/blob/main/KDD2021/UK_RMSE.png" width="400" height="360"/><br/>

We have experimented with the adjacent wards missing pattern for Cancer in Figure 1, with the following results. The results show that our model still works best
<img src="https://github.com/WoodScene/Paper_pictures/blob/main/KDD2021/UK_RMSE.png" width="400" height="360"/><br/>
<img src="https://github.com/WoodScene/Paper_pictures/blob/main/KDD2021/UK_RMSE.png" width="400" height="360"/><br/>

5. Experimental supplement
* new baselines:

(1)	demographic-based linear regression

(2) demographic-based spatial average/mean

(3) method in quote [5] (CPH)

------------------------------------------------------------------------------------------------------------------------
The source code for Spatial-attention and Demographic-augmented Generative Adversarial Imputation Network for Online Population Health Data Reconstruction   
Thank you for your interest in our work, we have uploaded the code for all models here.

## Requirements
Install python, tensorflow. We use Python 3.7, Tensorflow 1.14.0.

## Data preparation
The Chronic Diseases Prevalence Dataset is open according to [here](https://digital.nhs.uk/data-and-information/publications/statistical/quality-and-outcomes-framework-achievement-prevalence-and-exceptions-data)

The London Demographic Dataset is open according to [here](https://data.london.gov.uk/dataset/gla-population-projections-custom-age-tables)

## Run
All the hyper-parameters and steps are included in the ./SDA-GAIN/main.py file, you can run it directly.

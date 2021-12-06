# Spatial-attention and Demographic-augmented Generative Adversarial Imputation Network

## Update: Experimental results in rebuttal
### 1. About data missing rates and missing patterns

The experimental results at low missing rates (40% missing) are shown below. From the results we can see that the advantage of SDA-GAIN is reduced but still as good as other baseline methods.

<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/missingrate40_RMSE.png" width="480" height="360"/><br/>

<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/missingrate40_MAPE.png" width="480" height="360"/><br/>


We have experimented with the adjacent wards missing pattern for Cancer in Figure 1, with the following results. The results show that our model still works best.


### 5. Experimental supplement
* new baselines: demographic-based linear regression, demographic-based spatial average/mean,  and method in quote 5 (CPH). The results of the experiment were as follows.
* new ablation experiment SDA-GAIN3_ : Remove demographic data from the model. And the results show that the improvement comes both from the model architecture and the additional data access.
* experiments with other spatially structured dataset: US-Hypertension dataset which has a larger spatial granularity (https://www.cdc.gov/500cities/). And our model still performed consistently with the London dataset.

<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/US_RMSE.png" width="480" height="360"/><br/>

<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/US_MAPE.png" width="480" height="360"/><br/>

### 7. Discussion of other related work 
Here we have supplemented the experimental results of the [2] [3] method mentioned by R4. As can be seen from the results, our method still gives the best completion results.




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

# Spatial-attention and Demographic-augmented Generative Adversarial Imputation Network

## Update: Experimental results in rebuttal
### 1. About data missing rates and missing patterns

The experimental results at low missing rates (40% missing) are shown below. It is worth noting that 30% of the original data is missing and we need at least 10% of the data to verify the effect of the completions. So the minimum missing rate that can be set for the experiment is 40%. From the results we can see that the advantage of SDA-GAIN is reduced but still as good as other baseline methods.

<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/missingrate40_RMSE.png" width="480" /><br/>
<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/missingrate40_MAPE.png" width="480" /><br/>

We have experimented with the adjacent wards missing pattern for Cancer in Figure 1, with the following results. The results show that our model still works best.

<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/London_RMSE.png" width="480" /><br/>
<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/London_MAPE.png" width="480" /><br/>

### 5. Experimental supplement
* new baselines: demographic-based linear regression, demographic-based spatial average/mean,  and method in quote 5 (CPH). The results of the experiment for CHD were as follows.

<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/new_baseline_RMSE.png" width="480" /><br/>
<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/new_baseline_MAPE.png" width="480" /><br/>

* new ablation experiment SDA-GAIN3_ : Remove demographic data from the model. And the results show that the improvement comes both from the model architecture and the additional data access.

<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/ablation_experiment_RMSE.png" width="480" /><br/>
<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/ablation_experiment_MAPE.png" width="480" /><br/>

* experiments with other spatially structured dataset: US-Hypertension dataset which has a larger spatial granularity (https://www.cdc.gov/500cities/). And our model still performed consistently with the London dataset.

<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/US_RMSE.png" width="480" height="360"/><br/>

<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/US_MAPE.png" width="480" height="360"/><br/>

### 7. Discussion of other related work 
Here we have supplemented the experimental results for CHD of the [2] [3] method mentioned by R4. As can be seen from the results, our method still gives the best completion results.

<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/related_work_RMSE.png" width="480" /><br/>
<img src="https://github.com/www22SDAGAIN/Paper_pictures/blob/main/related_work_MAPE.png" width="480" /><br/>


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

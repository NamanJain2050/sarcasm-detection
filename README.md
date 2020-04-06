# Sarcasm Detection in Reddit Comments

This repository showcases my work on sarcasm detection task. <br>
Problem description: Given raw comments from Reddit, we have to classify them as sarcastic or not. <br>
Dataset source: https://www.kaggle.com/danofer/sarcasm <br>
Paper referred: https://arxiv.org/abs/1610.08815

## Description of each notebook
1. prepare-data-csv.ipynb: Using raw data source to create usable data CSVs
2. Data cleaning and EDA.ipyb: Cleaning text and some Exploratory data analysis on our data
3. Modelling.ipynb: CNN model for text classification task

## Dataset details
We have a prepared a perfectly balanced dataset for our task.

<table>
  <tr>
    <th></th>
    <th>Sarcastic (1)</th>
    <th>Not sarcastic (0)</th>
  </tr>
  <tr>
    <td>Train</td>
    <td>400000</td>
    <td>400000</td>	
  </tr>
  <tr>
    <td>CV</td>
    <td>50000</td>
    <td>50000</td>
  </tr>
  <tr>
    <td>Test</td>
    <td>50000</td>
    <td>50000</td>
  </tr>
  <tr>
    <td>Total</td>
    <td>500000</td>
    <td>500000</td>		
  </tr>
</table> 

## Modelling
We've used 1D CNN models to extract features from raw texts and make classifications.
We've used combinations of three different kinds of features:
1. Content features from raw texts
2. Sentiment features using Transfer Learning. Model trained on twitter dataset. More information can be found here: https://github.com/NamanJain2050/semeval-2014-task-9/
3. Emotion features using Transfer Learning. Two models trained on two different datasets. More information can be found here: https://github.com/NamanJain2050/emotion-detection

### Model 1: Using only content features
Predictions made using only content features extracted from 1D CNN. Model architecture is as follows:
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/model_01.png" alt="model_01"/>
</p>
<b> Results of this model are as follows: </b>
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/model_1_cnf.png" alt="model_01"/>
</p>
We've achieved an F1-score of 0.7234 and we were able to classify 73.58% of sarcastic comments correcly.

### Model 2: Using content features + sentiment features
Predictions made using content features extracted from 1D CNN and sentiment features from pre-trained model. Model architecture is as follows:
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/model_02.png" alt="model_02"/>
</p>
<b> Results of this model are as follows: </b>
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/model_2_cnf.png" alt="model_02"/>
</p>
We've achieved an F1-score of 0.7179 and we were able to classify 71.78% of sarcastic comments correcly.

### Model 3: Using content features + emotion features
Predictions made using content features extracted from 1D CNN and emotion features from pre-trained model. Model architecture is as follows:
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/model_03.png" alt="model_03"/>
</p>
<b> Results of this model are as follows: </b>
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/model_3_cnf.png" alt="model_03"/>
</p>
We've achieved an F1-score of 0.7242 and we were able to classify 71.75% of sarcastic comments correcly.

### Model 4: Using content features + emotion features
Predictions made using content features extracted from 1D CNN and emotion features from pre-trained model. This time we'll use a different model trained for emotion features. Model architecture is as follows:
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/model_04.png" alt="model_04"/>
</p>
<b> Results of this model are as follows: </b>
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/model_4_cnf.png" alt="model_04"/>
</p>
We've achieved an F1-score of 0.7235 and we were able to classify 72.07% of sarcastic comments correcly.


### Model 5: Using content features + sentiment features + emotion features
Predictions made using content features extracted from 1D CNN, sentiment features and emotion features extracted from pre-trained models. Model architecture is as follows:
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/model_05.png" alt="model_05"/>
</p>
<b> Results of this model are as follows: </b>
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/model_5_cnf.png" alt="model_05"/>
</p>
We've achieved an F1-score of 0.7222 and we were able to classify 70.71% of sarcastic comments correcly.

### Model 6: Using content features + sentiment features + emotion features
Predictions made using content features extracted from 1D CNN, sentiment features and emotion features extracted from pre-trained models. Model architecture is as follows:
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/model_06.png" alt="model_06"/>
</p>
<b> Results of this model are as follows: </b>
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/model_6_cnf.png" alt="model_06"/>
</p>
We've achieved an F1-score of 0.7215 and we were able to classify 72.1% of sarcastic comments correcly.

## Summary of results
<p align="center">
  <img src="https://github.com/NamanJain2050/sarcasm-detection/blob/master/images/summary.png" alt="summary"/>
</p>

## Conclusions
We've seen that adding emotion and sentiment features from pretrained models have <b> degraded </b> our results. <br>
Possible reason(s):
1. Models were trained on much smaller datasets as compared to our SARC dataset

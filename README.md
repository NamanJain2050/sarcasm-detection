# Sarcasm Detection in Reddit Comments

This repository showcases my work on sarcasm detection task. <br>
Problem description: Given raw comments from Reddit, we have to classify them as sarcastic or not. <br>
Dataset source: https://www.kaggle.com/danofer/sarcasm <br>
Related Medium article: https://tinyurl.com/t632sh9

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

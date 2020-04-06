# Sarcasm Detection in Reddit Comments

This repository showcases my work on sarcasm detection task. <br>
Problem description: Given raw comments from Reddit, we have to classify them as sarcastic or not. <br>
Dataset source: https://www.kaggle.com/danofer/sarcasm <br>
Related Medium article: https://tinyurl.com/t632sh9

## Description of each notebook
1. prepare-data-csv.ipynb: Using raw data source to create usable data CSVs
2. Data cleaning and EDA.ipyb: Cleaning text and some Exploratory data analysis on our data
3. Modelling.ipynb: CNN model for text classification task

## Dataset details:

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

# Yachay.ai Geolocation Prediction from Tweets


## Purpose

This was a project developed during an externship at yachay.ai. This project aims to predict the geolocation of tweets with deeplearning techniques. 

## Project Overview
- Preprocssed and performed EDA on dataset containing 500000 tweets from North America
- Developed and trained multiple Bert and electra regression and classificaton models to geolocate the tweet data
- The regression model uses haversine distance in km as its main loss metric while the classification model uses accuracy 

- The classification model divides North America into 10 regions using K-means. See image below.
![image](https://github.com/hugotomita1201/yachay.ai_project/assets/70402339/a6149a39-6b9d-4181-b362-d7e4ccf4b49e)

## Results

Various models were tested on different sets of data. The dataset labeled text + user_id + timestamp had the text data, a label encoded user_id, and an hourly timestamp.

The highest performing model was the electra-small-discrimminator on tweet data only with an accuracy of 36% and a mean haversine distance of 1363 km
![image](https://github.com/hugotomita1201/yachay.ai_project/assets/70402339/9b3e7be0-91c8-4fd8-a5db-a6f834667fb8)


datasets: 
grouped_data_w_text_features: this csv file contains the modified dataset with additional time and user_id total tweetcount text features
ungrouped_data: this csv file is an unmodified dataset with cluster_ids
https://drive.google.com/drive/folders/17w4EKx05hWMLC2opzLCT09bJrEMS8OqR?usp=drive_link

electra_class_grouped: this notebook runs an electra classification model on the modified data\
electra_class_ungrouped: this notebook runs the same electra model but on data that is not modified\
electra_reg: this is a modified regression electra model that predicts lat lng coordinates

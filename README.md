<h1 align="center">
SOLAR AND WIND ENERGY PREDICTION
</h1>

<p align="center">
<a href="https://www.youtube.com/watch?v=BQPUwUDnKRE" target="_blank">Video Demo</a>
</p>

SOLAR AND WIND ENERGY PREDICTION using Machine and Deep Learning models


   
<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#salient-features">Salient Features</a></li>
       <li><a href="#built-with">Built With</a></li>
        <li><a href="#compatible-platforms">Compatible Platforms</a></li>    
      </ul>
    </li>
    <li>
      <a href="#description">Description</a>
      <ul>
        <li><a href="#dataset">Dataset</a></li>
        <li><a href="#data-preprocessing">Data Preprocessing</a></li>
         <ul>
            <li><a href="Removing Null Values">Removing Null Values</a></li>
            <li><a href="Correlation analysis">Correlation analysis</a></li>
            <li><a href="Feature Importance">Feature Importance</a></li>
         </ul>
      </ul>
    </li>
    <li>
      <a href="#results">Results</a>
    </li>
    <li>
      <a href="#User Interface">User Interface</a>
    </li>
    <li>
      <a href="#team">Team</a>
    </li>
    
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About the project
* Solar energy is one of several sustainable sources that is becoming increasingly important in the energy sector due to its potential to cut carbon emissions and counteract growing electricity prices. The main issue with solar energy is that it cannot be used due to the constantly shifting and unpredictable weather, cloud cover, climate, and seasons. As a result, solar energy generation varies. Therefore, resource planners and businesses are looking for models that take these uncertainties into account for the daily design and management of solar energy production, which could enable them to meet consumer demand and supply regardless of weather conditions.
* Weather complexity makes accurate synthesis of wind output difficult, and commercial confidentiality means that historical data is frequently limited. We present and validate a model for simulating the hourly power output of wind and solar energy farms. 

### Salient Features
Predicts real-time solar and wind energy. Accuracy, mean square error, root mean square error, mean absolute error are calculated for each algorithm and different hyperparameters and the best one is chosen.

### Compatible Platforms
Laptops, Desktops and Tablet PCs

### Built With

### Tech stack used
* Frontend: HTML, CSS, Bootstrap
* Backend: JavaScript, Python
* Prediction models: ML/DL models
* ML Models: Lasso Regression, Ridge Regression, Decision Tree, SVM, Random Forest
* DL Model: LSTM


## Description
### Dataset 
Data was collected from https://open-power-system-data.org/ which is a free open source platform with data on power systems for 37 European countries. But we chose to focus on a specific country, Germany, due to having the highest proportion of renewable energy than any other country(about 46 percent of its energy come from solar, wind, biomass) and hence it is a good indicator of where the rest of the world is headed. The data file contained about 16 variables like utc_time stamp,solar capacity,wind capacity,solar profile, wind profile,wind_onshore, wind_offshore profile.

### Data Preprocessing
#### Removing null values
1.For solar generation actual, wherever there is a null value, it has been filled with the value for a day before.For the first day of the month, since   there is no previous day value, it has been filled with 0 assuming there is no solar generation before 6 am.Then we replaced leftover Nan values with mean of the data of solar generation actual 
2. For wind generation actual, wherever there is a null value, it has been filled with the mean value of the entire wind generation actual column.

#### Correlation analysis 
It show that some features are more correlated to target variables. Solar profile is most correlated with solar generation output. In case of wind energy, wind profile, wind onshore profile, wind onshore generation followed by wind offshore profile and wind offshore generation.

![image](https://user-images.githubusercontent.com/87893594/211166795-6f554565-dee5-4d3d-8998-0795c909fd10.png)

#### Feature Importance
Along with correlation analysis, feature importance was used to select the most appropriate features of our dataset for robust model training. Useless data must be removed for low bias. It is a technique that calculates the score of each input feature. The score indicates the importance of that feature. 

## Results
We applied machine learning algorithms like Ridge and Lasso Regression, SVM, Random Forest, Decision Tree and LSTM on our data. We tested our models on various regression metrics like Accuracy, mean square error, root mean square error etc with  different hyperparameters. After considering these models, we found that SVM model was best suited for wind energy and Random forest for solar energy.Amongst Deep learning models, LSTM gave the best accuracy 0f about 98.2% for solar energy.

![WhatsApp Image 2023-01-08 at 12 51 55 PM](https://user-images.githubusercontent.com/74909133/211185941-6d9292c6-acee-476a-9dd6-467f804c80b5.jpeg)
![WhatsApp Image 2023-01-08 at 12 51 55 PM (1)](https://user-images.githubusercontent.com/74909133/211185945-1c4de132-e170-4307-b1b0-94b7b6e4fef5.jpeg)

![WhatsApp Image 2023-01-08 at 12 51 55 PM (2)](https://user-images.githubusercontent.com/74909133/211186083-d5179172-9220-4d6b-b62a-08490c9e6b7e.jpeg)

<h6> LSTM graph showing true values and predicted values </h6>





## A possible User Interface 
<img width="1440" alt="solar predictor" src="https://user-images.githubusercontent.com/74909133/211185851-e1f6a5cb-2258-4bef-ae44-5aa2d266cc92.png">
<img width="1440" alt="wind_predictor" src="https://user-images.githubusercontent.com/74909133/211185854-f65a083c-1ef2-4a82-b974-cde3e9249800.png">



### Team
- Mehak Aggarwal
- Sonanshi Goel
- Shambhavi Rai
- Princy Singhal

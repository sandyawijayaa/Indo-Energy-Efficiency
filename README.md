# Indo-Energy-Efficiency
Group project for my Fall '23 course Data, Environment, and Society (ENERES131)

## Motivation
Indonesia is a diverse archipelago at the crossroads of the Pacific and Indian oceans and a key player in Southeast Asia's economic landscape. With the constant surge in population and economic activities, there is a demand for a keen assessment of energy needs -- specifically, the efficiency of energy generation.

## Project Questions
_Our aim is to not only predict Indonesia's 2024 energy efficiency by province using socioeconomic, demographic, and environmental features from 3 years prior -- but also whether it's better to predict this using 2 regression models (Q1 & Q2) or 1 classification model (Q3)._ To answer this question, we will break it up into three prediction questions. 
1. Regression model: Predict its electricity **generation**.
- Linear Regression, Ridge Regression
2. Regression model: Predict provinces' energy **capacities**.
- Linear Regression, Ridge Regression, LSTM, and ARIMAX
3. Classification model: We will generate a new target variable that will split up the **efficiency** rates into 3 classes: 0 if efficiency is less than 0.33, 1 if efficiency is 0.33 (inclusive) and 0.6 (non-inclusive), and 2 if efficiency is 0.6 or higher. Then, we will make a classification model to predict this target variable.
- KNN, Random Forest, and Decision Trees

After the completion of these three questions, we will divide the predicted energy generation (Q1) by the predicted capacity (Q2) for each province in each predicted year. We then apply our classification function to each datapoint, assigning 0s, 1s and 2s as we did in our classification model. This will allow us to directly compare the efficiency class of each province in each year based on if we performed the classification before (Q1 & Q2) or after (Q3) modelling.

## Conclusion
Our best regression model was Ridge Regression (RMSE of ~2000) and our best classification model was Random Forest (accuracy of ~70%). Backed by research, we defined energy generation to be 'not efficient' if it reaches 33% or below maximum capacity, 'efficient' if its between 33% and 60% efficient, and "very efficient if above 60%.

While our Ridge Regression model predicted 30/34 provinces to have efficient energy capacity (above 33%), our Random Forest classification model predicted only 15/34. On average, the predicted 2024 ratio of energy generation to capacity is 0.45 -- meaning we predict that in 2024, energy generation will perform at 45% of the maximum capacity. This is considered efficient: our prediction states that Indonesia as a country will have efficient energy generation in 2024.

#### Collaborators: Sandya Wijaya, Ethan Chien, Emna Sellami, Amitesh Gargapati (all contributions listed in Final Project Notebook.ipynb)

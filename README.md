**Water Quality Analysis and Prediction**
By:-

Nihar  (220381) 
Divyanshu (220375) 
Piyush Garg (220491) 
Nirbhay (220412) 

**Abstract** 
The process of attempting to analyze and predict  changes in water quality parameters is known 
as water quality analysis and prediction. Accurate analysis regarding water quality could lead 
to significant improvements in managing water resources and mitigating potential hazards. In 
recent years, the application of sentiment analysis techniques to water quality prediction has 
gained traction. This report presents an analysis of water quality predictions using machine 
learning models based on physicochemical parameters. Data spanning from 2017 to 2021 from 
various monitoring stations across different states were collected and analyzed. Four key 
parameters - Dissolved Oxygen, pH, Biochemical Oxygen Demand (BOD), and Nitrate - were 
used as features to predict water quality classes. The Support Vector Classifier (SVC) machine 
learning model was trained and applied to the datasets to analyze and predict the quality of 
water at different monitoring locations. The results revealed insights into the distribution of 
predicted water quality classes, highlighting areas of concern for water pollution and 
environmental protection. The findings underscore the importance of continued monitoring and 
assessment of water quality for public health and environmental sustainability. 

**INTRODUCTION**
Water quality prediction is of paramount importance for ensuring the safety and sustainability of our natural resources. With data collected spanning from 2017 to 2021 from various monitoring stations across different states, this project endeavors to analyze and predict water  quality levels. Four critical parameters - Dissolved Oxygen, pH, Biochemical Oxygen Demand (BOD), and Nitrate - serve as the foundational features for this predictive analysis. Stakeholders in water management must have access to accurate predictions to safeguard public health and environmental integrity. Water quality analysts aim to ascertain the highest standards in water quality for the well-being of communities and ecosystems. Utilizing the Support Vector Classifier (SVC) machine learning model, this study applies advanced computational techniques to the datasets, aiming to forecast water quality across different monitoring locations. By discerning patterns and trends in water quality data, this research contributes valuable insights into the distribution of predicted water quality classes. The implications of this study extend far beyond data analysis; they underscore the urgent need for proactive measures in combating water pollution and advocating for environmental protection. By identifying areas of concern and potential risks, stakeholders can prioritize resource allocation and intervention strategies to mitigate environmental degradation and ensure sustainable water management practices. In the subsequent sections of this report, we delve into the methodology employed, the results obtained, and the implications of our findings. Through rigorous analysis and interpretation, this study seeks to inform policy-makers, environmentalists, and the general public about the critical importance of continued monitoring and assessment of water quality for the collective 
well-being of society and the environment. 
 
 
**DATASET DESCRIPTION** 
 Dataset 
The dataset utilized has been sourced from the official website of the Government of India, specifically the "Central Pollution Control Board." This dataset encompasses six significant rivers: Ganga, Beas, Brahmaputra, Godavari, Krishna, and Satluj. Spanning a period of five years, from 2017 to 2021, this comprehensive dataset serves as a valuable resource for analyzing and understanding the water quality trends and dynamics within these vital water bodies. 
Year Number of Rows  Number of Columns 
**2017 202 9 
2018 209 9 
2019 249 9 
2020 237 9 
2021 263 9** 
 
• **station_code**: Unique numeric code assigned to each monitoring station location. 
• **location:** The specific name of the location where the monitoring station is situated. Locations are along major rivers like Ganga, Brahmaputra, Godavari, Krishna, Beas, and Satluj. 
• **state:** State in India where the monitoring location is situated. 
• **DissolvedOxygen**: Measure of the concentration of dissolved oxygen gas in the water body (in mg/L). 
• **pH:** Measures the acidity or basicity of the water on a scale of 0-14. 
• **BOD:** Biochemical Oxygen Demand is a measure of the amount of dissolved oxygen required/consumed by microorganisms to break down organic matter present in the water. Higher values indicate more organic pollution load. 
• **Nitrate:** Measures the concentration of nitrate in the water (in mg/L). Nitrates can come from agricultural runoff, sewage, etc. 
• **Latitude:** The latitude coordinate of the monitoring location. 
• **Longitude:** The longitude coordinate of the monitoring location. 
• **year:** Year in which the measurements were taken. 
In addition to the primary water quality monitoring data, an auxiliary dataset has been furnished, consisting of 1,755 rows of observations and 5 columns of variables. The inclusion of this secondary dataset serves the purpose of enriching the training process for the development of predictive models pertinent to water quality assessment. By integrating this supplementary data, we aim to enhance the depth and accuracy of our analytical endeavors in understanding and managing water quality dynamics.

**EDA**

![image](https://github.com/user-attachments/assets/bd848866-f7ed-43c9-9376-b1d1c6d02ce2)

![image](https://github.com/user-attachments/assets/e3d28e6e-9576-4b25-8355-b05da99ef275)

![image](https://github.com/user-attachments/assets/8f1cc3bc-5154-4365-bfa4-70935696b0e4)



**METHODOLOGY**

**1. Data Loading and Exploration:** 
o The code loads water quality data from an Excel file (water_quality.xlsx) using pandas. 
o It performs basic data exploration, such as displaying a sample of the data, checking the shape (number of rows and columns), obtaining information about 
the data types, and calculating descriptive statistics. 
o It also checks for duplicate entries and counts the number of instances for each class in the 'Quality' column. 
**2. Data Visualization:**  
o The code creates a bar plot to visualize the distribution of water quality classes ('Quality') using matplotlib and seaborn libraries. 
o It also generates a heatmap to show the correlation between different water quality parameters. 
**3. Data Preprocessing:**  
o Manual label encoding is performed on the 'Quality' column, mapping string labels to numerical values. 
o The code visualizes the label mapping for better understanding. 
**4. Feature Selection and Split:**  
o The features 'DissolvedOxygen', 'pH', 'BOD', and 'Nitrate' are selected as predictors (X), while 'Quality' is chosen as the target variable (y). 
o The data is split into training and testing sets using train_test_split from scikit-learn. 
**5. Feature Scaling:**  
o The predictor variables are scaled using StandardScaler from scikit-learn to ensure consistent scales across features. 
**6. Model Building and Evaluation:**  
o The code defines a function model_building to fit various machine learning models, make predictions, and calculate evaluation metrics like accuracy score and classification report. 
o Several models are trained and evaluated, including Logistic Regression, Random Forest Classifier, Decision Tree Classifier, and Support Vector Classifier (SVC). 
o The models' performance is evaluated using accuracy scores and classification reports. 
o Confusion matrices are generated for each model and visualized using heatmaps. 
**• Random Forest**
Applications for classification and regression commonly use supervised machine learning techniques like random forest. When doing regression on different data, it builds decision trees and utilises their average for categorization and majority vote for voting. There are two models: the Random Forest Classifier, an ensemble technique in which the model is built from several little decision trees, or estimators, each of which generates a separate set of predictions. A more precise forecast is made by combining all of the estimators' estimations rather than just one tree. Using supervised learning, the Random Forest Regressor employs ensemble learning techniques for regression. The ensemble prediction of a machine learning algorithm is created by merging the predictions of many machine learning algorithms. By combining predictions from various algorithms, it generates predictions that are more accurate than those from a single model. 
**• Logistic Regression** 
Supervised machine learning techniques commonly utilize logistic regression for classification tasks. It models the probability of a binary outcome by fitting data to a logistic curve. Logistic regression operates by estimating coefficients for each feature and applying them to a logistic function to predict the probability of an event. Unlike random forest, which utilizes an ensemble of decision trees, logistic regression is a single-model approach. It calculates the probability of a binary outcome using a linear combination of features and applies a logistic function to map this result to a range between 0 and 1, representing the probability of belonging to a particular class. 
 
**• Decision Tree Classifier** 
Classification and regression tasks frequently employ supervised machine learning methods like decision trees. Decision Tree Classifier, akin to Random Forest, operates by constructing decision trees on diverse data sets. Each tree provides its own predictions, which are then combined to produce a more accurate forecast. Similarly, Decision Tree Regressor utilizes ensemble learning techniques to generate regression predictions. By amalgamating predictions from multiple decision trees, it achieves greater accuracy compared to individual models. 
 
**• Support Vector Classifier (SVC**) 
Supervised machine learning commonly employs support vector classifier (SVC) for classification tasks. SVC constructs decision boundaries based on training data points to classify new instances. It separates classes by finding the hyperplane that maximizes the margin between them. The SVC model utilizes a subset of training data points, known as support vectors, to define the decision boundary. It aims to maximize the margin while minimizing classification errors. By using supervised learning, SVC ensures accurate classification by finding the optimal hyperplane that best separates different classes in the feature space. 

**7. Model Selection and Testing:**  
o The SVC model is selected, and its performance is further evaluated by making predictions on separate datasets for the years 2017, 2018, 2019, 2020, and 2021. 
o The predictions are added to each dataset as a new column ('Predicted_Quality'), and the distribution of predicted water quality classes is analyzed.

**8. Visualization on Maps:**  
o For each year (2017-2021), the code creates an interactive map of India using the folium library. 
o The monitoring locations are plotted on the map as markers, with colorsrepresenting different predicted water quality classes. 
o Marker clusters are used to group nearby markers for better visualization. 

**9. COVID-19 Period Analysis:**  
o The code filters the data for the years 2019, 2020, and 2021, representing the COVID-19 period. 
o It creates a count plot using seaborn to visualize the distribution of water quality classes during this period, grouped by year. 
The methodology covers data loading, exploration, visualization, pre-processing, feature selection, model building, evaluation, prediction, and spatial visualization on maps. Additionally, it includes a specific analysis of the water quality distribution during the COVID-19 period (2019-2021). 

![image](https://github.com/user-attachments/assets/c3baae79-0f6b-4e23-a51e-99c9dd518d2f)



**Results** 
Model/Algorithm Performance 
We conducted a comprehensive analysis of water quality prediction using several classification models: Logistic Regression, Random Forest Classifier, Decision Tree Classifier, and Support Vector Classifier (SVC). Each model was evaluated based on key performance metrics including **accuracy, precision, recall, and F1-score.** 
Here's a detailed comparison of the results obtained from each model: 
Scores obtained for each of these models

Model Accuracy Precision Recall F1-score 
![image](https://github.com/user-attachments/assets/5fb8aed2-3654-4d59-8d36-cfc38193a6d8)


**Comparative Analysis**
Among these models, the Support Vector Classifier (SVC) demonstrated the highest accuracy 
of **94%** and achieved the highest precision, recall, and F1-score. Therefore, we selected the 
SVC model as our final predictor for water quality. 
Reasons for Fluctuation in Water Quality: 
The analysis of water quality fluctuations revealed several contributing factors: 
1. COVID-19 Pandemic: During the COVID-19 pandemic, reduced industrial activities 
and human movements might have positively impacted water quality due to decreased 
pollution levels. 
2. Industrial Pollution: Industrial effluents containing pollutants such as heavy metals, 
chemicals, and organic matter can contaminate water sources, leading to predictions of 
polluted water quality. 
3. Agricultural Waste: Runoff from agricultural fields carrying fertilizers, pesticides, 
and other chemicals can enter water bodies, affecting water quality. 
4. Natural Factors: Environmental factors such as rainfall, temperature variations, and 
seasonal changes can also influence water quality fluctuations. 
The study highlights the importance of employing machine learning models for predicting 
water quality and understanding the underlying factors contributing to its fluctuations. By 
leveraging advanced analytics, policymakers and environmental agencies can make informed 
decisions to mitigate pollution and ensure sustainable management of water resources.
![image](https://github.com/user-attachments/assets/d192b906-e82e-4bc6-a4a6-725bbdd53867)


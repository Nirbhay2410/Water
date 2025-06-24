Water Quality Analysis and Prediction 
By:-
Nihar  (220381) 
Divyanshu (220375) 
Piyush Garg (220491) 
Nirbhay (220412) 
 
  
**Abstract **
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
 
 
  
**INTRODUCTION **
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


## Early Detection of Diabetes Using  Machine Learning

## Problem Background
Diabetes, a rapidly escalating global health issue, affected 422 million people worldwide as of 2018 (WHO).
The number of people affected is expected to have increased significantly since then.
Approximately 50% of all people with diabetes are undiagnosed due to its long-term asymptomatic phase.
In the United States, 8.5 million people (23.0% of adults) are undiagnosed. (June 29, 2022)
Early detection is vital for clinically meaningful outcomes, requiring careful assessment of both common and less common symptoms.

## The Challenge
Currently, there is a lack of efficient methods to predict the likelihood of developing diabetes.
The unique asymptomatic phase of diabetes presents a significant challenge for early detection and intervention.


## My Approach
We used data mining classification techniques and machine learning models to predict the likelihood of developing diabetes.
A dataset of 520 instances from Sylhet Diabetes Hospital in Sylhet, Bangladesh, collected via direct questionnaires, will serve as the basis for our model.
Tools: Alteryx for data preparation and blending, Tableau for data visualization and exploration, and machine learning for predictive modelling and analysis.

## Objective
To leverage the power of Alteryx, Tableau, and Machine Learning to create a robust risk prediction model.
The ultimate goal is to facilitate the early detection of diabetes, thus enabling timely interventions and improved patient outcomes.

## Data 

<img width="643" alt="snip" src="https://github.com/juvi-coder/Diabetes_Early_Prediction/assets/100660932/926a6906-3f8b-48da-9398-ff70d7c9b3b3">


## Data Input

<img width="378" alt="EDA" src="https://github.com/juvi-coder/Diabetes_Early_Prediction/assets/100660932/a8a3d846-0bec-405e-a2a4-f32c75fea1c4">

**Data Input **

In Alteryx, I have imported the Diabetes dataset using the Input Data tool. The only modification I've made during this data input stage was to adjust the column names to follow the snake_case format.

The browse tool here summarized and graphed all the variables.  



**Data Preparation Steps:**

<img width="419" alt="sd" src="https://github.com/juvi-coder/Diabetes_Early_Prediction/assets/100660932/5f3e0ef6-7c5d-48d9-9810-1ad506e18851">

**Age Transformation:** Utilizing the Formula tool, I've transformed the Age variable, which is continuous and ranges from 16 to 90, into an ordinal variable. The new Age buckets are: [16-35], [36-45], [46-55], [56-65], and [66>].

**Class Variable Transformation:** The Class variable has been converted into a binary format, where 'Positive' is represented by 1 and 'Negative' is represented by 0.

**Gender Variable Transformation:** Similarly, the Gender variable has been transformed into a binary format, where 'Male' is represented by 0 and 'Female' is represented by 1.

**Categorical Variables Transformation:** With the help of the Multi-Field Formula tool, I've converted all the remaining categorical variables into binary variables, assigning 'True Class' as 1 and 'False Class' as 0.

**Selection Tool for Conversion:** To finalize the data preparation for statistical testing and model building, I've used the Selection tool to convert all variables into numerical format.

These refined steps provide a clear description of the data preparation process carried out in Alteryx.
## CHi Square
<img width="335" alt="chi" src="https://github.com/juvi-coder/Diabetes_Early_Prediction/assets/100660932/ba43f52c-5712-4bec-8dd8-4b41278b1dc2">




I utilized the Contingency Tables tool in Alteryx to conduct Chi-Square tests. This was done to determine if there are significant relationships between the categorical independent variables and the target variable.

From the tests, all variables except for 'Itching', 'Delayed_healing', and 'Obesity' demonstrated significant relationships with the target variable.


## Final Varaibles for modelling 
<img width="1009" alt="Screenshot 2023-05-23 at 9 34 39 AM" src="https://github.com/juvi-coder/Diabetes_Early_Prediction/assets/100660932/b9d5b40e-3080-47b9-aa17-0a3f1547135f">



## Modeling Workflow
<img width="1061" alt="Modeling Workflow" src="https://github.com/juvi-coder/Diabetes_Early_Prediction/assets/100660932/2375cb30-950f-4142-9727-cbf0123b3490">

## Final Results
<img width="465" alt="Capture4" src="https://github.com/juvi-coder/Diabetes_Early_Prediction/assets/100660932/09bf7cb4-b220-4ce1-b74d-19c55110dfb7">


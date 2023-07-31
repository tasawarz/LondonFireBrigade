# LondonFireBrigade
**Data Analyst Portfolio - Fire Incident Analysis Report**

**Introduction:**
The ability to identify changes and patterns in fire incidents as they occur is highly desirable, especially if they are unexpected. The frequency of various types of fire incidents may vary with the change of season, time of day, day of the week, geographical hierarchies, building infrastructure, and property types. These changes can be modeled and predicted to some extent, which is crucial for preventing further incidents. This report aims to explore the degree to which statistical techniques and data mining tools can assist the London Fire Brigade in detecting changes and demonstrate the insights gained from the dataset available.

The dataset used in this report has been provided by the London Fire Brigade (LFB) and is open-source data. It contains incidents reported in the city of London from 2017 to 2021, categorized into three types: False alarm, Special Services, and Fire. The dataset is organized based on geographical hierarchies, including administrative and statistical hierarchies.

**Business Understanding:**
The dataset contains various attributes, such as location, incident type, property information, number of pumps arriving, and incident cost. Several business questions are addressed in this report, including:

1. Analyzing trends of incidents categorized by incident group over the last 5 years.
2. Examining the influence of time (HourOfCall) on incident numbers and their categories.
3. Identifying the type of incidents that usually occur in different property categories.
4. Exploring the relationship between IncidentGroup, PropertyCategory, and HourOfCall.
5. Assessing the accuracy of predicting False Alarms.
6. Predicting the cost incurred based on the number of incidents.

**Data Preparation:**
The dataset initially contained 493,000 rows, representing incidents reported in the last 5 years in London. The data preparation involved filtering the dataset for the specific borough, which is Lambeth in this report. Attribute names were checked and modified to meet SAS Studio requirements. Irrelevant attributes were removed, and missing values were handled.

**Data Insights using SAS:**
The dataset was uploaded to SAS Studio and integrated into SAS Enterprise Miner to deduce useful results. Explore functions were utilized to check for data insights, outliers, data types, and missing values.

**Clustering:**
Clustering was applied to identify groups of similar objects in the dataset. It involved IncidentGroup, PropertyCategory, and HourOfCall to create meaningful clusters representing False Alarms, Special Services, and Fires.

**Predictive Analysis:**
Two predictive models were developed: Decision Tree Model and Regression Model.

1. **Decision Tree Model:** This model was used to predict the accuracy of False Alarms. Clustering was performed to understand the relationship between IncidentGroup, PropertyCategory, and HourOfCall. The model's misclassification rate was 44%, indicating 56% accuracy.

2. **Regression Model:** The regression model predicted the cost incurred on incidents. PumpHoursRoundUp was the input, and the model's performance was assessed based on the Average Square Error.

**Model Comparison:**
The Decision Tree Model was found to outperform the Regression Model based on their respective misclassification rates and Average Square Errors.

**Conclusion:**
This report analyzed the London Fire Brigade dataset, focusing on fire incidents. The predictive models provided insights into the accuracy of False Alarms and the cost incurred on incidents. However, due to the nature of fire incidents and the consequences they carry, further measures need to be taken beyond relying solely on these models. Recommendations include installing devices to inform the LFB about incident severity to reduce False Alarms and associated costs. Implementing such mechanisms will require careful planning and effort, but it is crucial for enhancing incident response and prevention strategies.

# LondonFireBrigade
**Data Analyst Portfolio - Fire Incident Analysis Report**

**Introduction:**
The ability to identify changes and patterns in fire incidents as they occur is highly desirable, especially if they are unexpected. The frequency of various types of fire incidents may vary with the change of season, time of day, day of the week, geographical hierarchies, building infrastructure, and property types. These changes can be modeled and predicted to some extent, which is crucial for preventing further incidents. This report aims to explore the degree to which statistical techniques and data mining tools can assist the London Fire Brigade in detecting changes and demonstrate the insights gained from the dataset available.

The dataset used in this report has been provided by the London Fire Brigade (LFB) and is open-source data. It contains incidents reported in the city of London from 2017 to 2021, categorized into three types: False alarm, Special Services, and Fire. The dataset is organized based on geographical hierarchies, including administrative and statistical hierarchies.

**Business Understanding:**
The dataset contains various attributes, such as location, incident type, property information, number of pumps arriving, and incident cost. Several business questions are addressed in this report, including:

1. Analyzing trends of incidents categorized by incident group over the last 5 years.
2. Examining the time series analysis. 
3. Assessing the accuracy of predicting False Alarms.
4. Geographically visualizing the incidents.
5. Predicting the number of pumps attending.


**Data Preparation:**
The dataset initially contained 493,000 rows, representing incidents reported in the last 5 years in London. The data preparation involved filtering the dataset for the specific borough, which is Lambeth in this report.  Irrelevant attributes were removed, and missing values were handled.

**Temporal Analysis:** Investigate how the frequency of fire incidents changes over time. This could involve analyzing trends by season, time of day, and day of the week to identify patterns in which incidents are more likely to occur. Temporal analysis can also help identify any significant changes or anomalies in the occurrence of fire incidents over the years.

**Spatial Analysis:** Explore the geographical distribution of fire incidents. This could include mapping the incidents and analyzing how incidents vary across different geographical hierarchies in the city of London. 

**Statistical Analysis:** Use statistical techniques to identify trends, correlations, and anomalies within the data. For example, performing time series analysis to detect seasonal patterns or using regression analysis to identify factors that may contribute to a higher likelihood of certain types of incidents.

**Regression Analysis**
Based on the correlation matrix provided, the following variables might be considered for inclusion in the regression analysis:

NumStationsWithPumpsAttending: Positive correlation with NumPumpsAttending.
PumpCount: Positive correlation with NumPumpsAttending.
FirstPumpArriving_AttendanceTime: Negative correlation with NumPumpsAttending.
SecondPumpArriving_AttendanceTime: Negative correlation with NumPumpsAttending.

OLS Regression results:
The R-squared value is approximately 0.819. This means that about 81.9% of the variance in the dependent variable 'NumPumpsAttending' is explained by the predictor variables included in the model. The regression model shows a reasonably good fit and indicates that the number of pumps attending incidents is influenced by the number of stations with pumps attending, the number of pumps attending, and the arrival times of the first and second pumps. However, it's essential to remember that regression analysis can only establish associations and not causal relationships, so further analysis, and domain knowledge might be needed to interpret the findings appropriately.

**Predictive Model**
Regression with NumPumpAttending being the target variable:

Mean Squared Error (MSE): 0.039741227723573726

The mean squared error measures the average squared difference between the actual values and the predicted values. A lower MSE indicates better model performance, as it represents how closely the model's predictions match the actual values. In your case, a value of 0.0397 suggests that your model's predictions are relatively close to the actual values.
R-squared (R²): 0.952077918786699

The R-squared value, also known as the coefficient of determination, indicates the proportion of the variance in the target variable that is explained by the model. It ranges from 0 to 1, where a higher value indicates that the model explains a larger portion of the variance. In your case, an R² value of 0.952 suggests that your model explains approximately 95.2% of the variance in the number of pumps attending fire incidents. This is a high value and indicates that your model is performing well in explaining the variation in the target variable.
Overall, these result

Random Forest Classifier with IncidentGroup being the target variable:
The overall accuracy of 80.48% suggests that the model is making accurate predictions.
The precision values vary across classes, with Class 0 having the highest (0.87) and Class 1 having the lowest (0.77).
Recall values indicate that the model performs better at identifying Class 0 (0.87) and Class 2 (0.84) instances compared to Class 1 (0.52).
The F1 scores provide a balance between precision and recall, showing the model's ability to balance both metrics.
The classification report offers insights into the model's performance across different classes and metrics.




# PHASE 3 PROJECT


# AIRLINES CUSTOMER SATISFACTION
![image](https://github.com/user-attachments/assets/0edf7ba6-a7e5-4e7d-912a-32b60203cc16)

## Overview
The dataset provided by Invistico Airlines contains valuable information about their customers' experiences and satisfaction levels. With an aim of predicting future customer satisfaction and improving service quality, this dataset encompasses various customer attributes and feedback on different aspects of their flights. The primary objectives of this dataset are to predict customer satisfaction and identify areas for service improvement.

## BUSINESS UNDERSTANDING
### Problem Statement
Airline companies operate in a highly competitive market where customer satisfaction significantly impacts loyalty and revenue. The goal is to understand the factors influencing customer satisfaction and predict whether a customer is satisfied or dissatisfied based on service and flight-related attributes.

### Objectives
1. Identify key factors that influence customer satisfaction.
2. Develop a predictive model to classify customers as "Satisfied" or "Dissatisfied."
3. Use insights from the model to inform business decisions and improve customer experience.

### Stakeholders
Airline Management: Use the insights to enhance service delivery and improve overall satisfaction scores.
Customer Service Team: Address main points identified through the analysis, such as delays or service quality.
Marketing Team: Target dissatisfied customers with specific campaigns to improve retention.
Operations Team: Optimize flight schedules and resource allocation to reduce delays and improve service metrics.

### Success Criteria
Improved customer satisfaction scores by addressing key drivers. Increased customer retention and loyalty as measured by repeat bookings. Reduced number of complaints or negative feedback. A predictive model with high accuracy, recall, and F1-score, ensuring effective identification of dissatisfied customers. Actionable insights derived from feature importance analysis, allowing stakeholders to prioritize improvements.

## DATA UNDERSTANDING
Our dataset, consists of 129,880 rows and 23 columns, there were no duplicated records, but there are 393 missing values in the 'Arrival Delay in Minutes' column. The data distribution is balanced across the various features. Upon closer examination, we identified a significant issue within certain 'rating' features. These features exhibit extremely low values in rate '0'. This poses a challenge for meaningful analysis. To address this, we decided to combine votes on rate '0' with votes on rate '1'. This step is essential as the majority of our features contain a limited number of 0 ratings compared to other ratings. Moreover, maintaining a rating scale from 1 to 5 is deemed appropriate for our analysis. There is strong correlation of 0.97 between "Departure Delay in Minutes" and 'Arrival Delay in Minutes'. This shows the two variables essentially represent the same information, and therefore, it is advisable to eliminate one of them. Given that 'Arrival Delay in Minutes' also contains missing values, we have decided to proceed with the removal of this variable. This simplification will streamline our analysis while retaining the essential information.

## Data Visualization
Based on the visualizations we observe that "Inflight entertainment" plays a key role in customer satisfaction, with a substantial difference between the satisfaction levels of those who are satisfied and dissatisfied. Therefore, it can be considered the most important feature. Additionally, "Seat comfort," "Online support," "Ease of Online booking", " On-board service,", "Leg room service" and "Online boarding" closely follow "Inflight entertainment" in terms of importance.
![image](https://github.com/user-attachments/assets/7d11b970-2f4a-4eec-92a0-3c8bd577b477)


This analysis assists in prioritizing which aspects of the airline's service may require particular attention for enhancing overall customer satisfaction.
To conclude, the distribution of customer ratings across the various features demonstrates varying degrees of influence on customer satisfaction. 'Inflight entertainment' takes precedence, followed by 'Seat comfort' and 'Online support,' while the remaining features show less pronounced effects.

## Data Preprocessing
Handle Missing Values Imputed missing values in the 'Arrival Delay in Minutes' column (393 entries).
Encode Categorical Variables:
Label Encoding: Applied to 'Gender', 'Customer Type', and 'Type of Travel' for binary categories,
One-Hot Encoding: Applied to 'Class' to create new columns for each class (Economy, Business, Economy Plus).
Merged '0' and '1' ratings in certain features e.g., 'Seat Comfort' to maintain a consistent 1-5 scale.
Scale Numerical Features: Standardized 'Age', 'Flight Distance', and 'Departure Delay in Minutes' using StandardScaler to normalize feature ranges.
Split Data: Divided the dataset into training 70% and testing 30% subsets for model development and evaluation.

## MODELING
Modeling is the process of building and training machine learning models to solve specific problems using preprocessed data. In this analysis, three models were developed and evaluated: Logistic Regression, Decision Tree, and Random Forest. Each model was trained on a dataset aimed at predicting customer satisfaction and assessed using metrics like accuracy and ROC-AUC.

-Logistic Regression:
Accuracy: 83.68%, Logistic Regression provided a straightforward and interpretable model. However, its performance was limited due to its linear nature, making it less effective in capturing complex relationships in the data.
-Decision Tree:
Accuracy: 93.84%, The Decision Tree outperformed Logistic Regression by handling non-linear data and identifying critical decision points. However, it showed a tendency to overfit, which may affect its generalization on unseen data.
-Random Forest:
Accuracy: 95.92%, Random Forest emerged as the best-performing model. By combining multiple decision trees, it reduced overfitting and improved accuracy and robustness. This ensemble approach excelled at capturing complex patterns in the dataset, making it the most reliable model for predicting customer satisfaction.
Overall, the Random Forest model is the most suitable for this task due to its superior accuracy and ability to generalize better than the other models. It provides actionable insights for stakeholders while ensuring reliable predictions.
![image](https://github.com/user-attachments/assets/8c5380e3-682e-404a-867e-01e69c380211)



## RECOMMENDATIONS
The most influential factors contributing to customer satisfaction are Seat Comfort, Inflight Entertainment, and Food and Drink. Prioritizing improvements in these areas can lead to a direct boost in customer satisfaction.

The Operations Team should focus on optimizing flight schedules to reduce delays and ensure smooth transitions from check-in to boarding.

The Marketing Team can use the insights to create campaigns targeting customers who are most likely to be dissatisfied, offering them 

Regularly gather customer feedback through surveys, social media, and review platforms. Use this feedback to update models and continuously adapt service offerings.

Empowering customer service representatives to offer personalized assistance could increase satisfaction, particularly in situations involving complaints or long wait times.


 ## CONCLUSION
 Our analysis demonstrates that several factors contribute to customer satisfaction in the airline industry. Notably, gender, customer type, and class play a significant role, with women, loyal customers, and those in the business class generally reporting higher satisfaction levels.

Furthermore, rating features such as "Inflight Entertainment" and "Seat Comfort" have emerged as crucial determinants of overall satisfaction. The "Inflight Entertainment" feature, in particular, has shown substantial influence.

Importantly, we discovered that age also influences satisfaction, with older passengers typically expressing higher satisfaction levels.

In our predictive modeling, the Random Forest algorithm yielded outstanding results, achieving an accuracy of 95%. This algorithm, along with feature importance analysis, confirmed the pivotal role of "Inflight Entertainment" and "Seat Comfort" in shaping customer satisfaction.

In conclusion, this analysis equips Invistico Airlines with insights to prioritize areas for improvement, specifically enhancing Inflight Entertainment and seat comfort. By addressing these aspects, the airline can foster higher customer satisfaction, bolster customer loyalty, and elevate its overall service quality.

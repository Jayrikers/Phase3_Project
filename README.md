# PHASE 3 PROJECT


# AIRLINES CUSTOMER SATISFACTION

## Overview
The dataset provided by Invistico Airlines contains valuable information about their customers' experiences and satisfaction levels. With an aim of predicting future customer satisfaction and improving service quality, this dataset encompasses various customer attributes and feedback on different aspects of their flights. The primary objectives of this dataset are to predict customer satisfaction and identify areas for service improvement.

## BUSINESS UNDERSTANDING
### Problem Statement
Airline companies operate in a highly competitive market where customer satisfaction significantly impacts loyalty and revenue. The goal is to understand the factors influencing customer satisfaction and predict whether a customer is satisfied or dissatisfied based on service and flight-related attributes.

### Objectives
1. Identify key factors that influence customer satisfaction. 2. Develop a predictive model to classify customers as "Satisfied" or "Dissatisfied." 3. Use insights from the model to inform business decisions and improve customer experience.

### Stakeholders
Airline Management: Use the insights to enhance service delivery and improve overall satisfaction scores.
Customer Service Team: Address pain points identified through the analysis, such as delays or service quality.
Marketing Team: Target dissatisfied customers with specific campaigns to improve retention.
Operations Team: Optimize flight schedules and resource allocation to reduce delays and improve service metrics.

### Success Criteria
Improved customer satisfaction scores by addressing key drivers. Increased customer retention and loyalty as measured by repeat bookings. Reduced number of complaints or negative feedback. A predictive model with high accuracy, recall, and F1-score, ensuring effective identification of dissatisfied customers. Actionable insights derived from feature importance analysis, allowing stakeholders to prioritize improvements.

## DATA UNDERSTANDING
Our dataset, consists of 129,880 rows and 23 columns, we observed no duplicated records, but there are 393 missing values specifically in the 'Arrival Delay in Minutes' column. The data distribution is largely balanced across the various features. Upon closer examination, we identified a significant issue within certain 'rating' features. These features exhibit extremely low values in rate '0'. This poses a challenge for meaningful analysis. To address this, we decided to combine votes on rate '0' with votes on rate '1'. This step is essential as the majority of our features contain a limited number of 0 ratings compared to other ratings. Moreover, maintaining a rating scale from 1 to 5 is deemed appropriate for our analysis. There is strong correlation of 0.97 between "Departure Delay in Minutes" and 'Arrival Delay in Minutes'. This shows the two variables essentially represent the same information, and therefore, it is advisable to eliminate one of them. Given that 'Arrival Delay in Minutes' also contains missing values, we have decided to proceed with the removal of this variable. This simplification will streamline our analysis while retaining the essential information.

## Data Visualization
Based on the visualizations we observe that "Inflight entertainment" plays a key role in customer satisfaction, with a substantial difference between the satisfaction levels of those who are satisfied and dissatisfied. Therefore, it can be considered the most important feature. Additionally, "Seat comfort," "Online support," "Ease of Online booking", " On-board service,", "Leg room service" and "Online boarding" closely follow "Inflight entertainment" in terms of importance.

This analysis assists in prioritizing which aspects of the airline's service may require particular attention for enhancing overall customer satisfaction.
To conclude, the distribution of customer ratings across the various features demonstrates varying degrees of influence on customer satisfaction. 'Inflight entertainment' takes precedence, followed by 'Seat comfort' and 'Online support,' while the remaining features show less pronounced effects.

## Data Preprocessing
We went through different preprocessing processes which included Encoding our data(using One-Hot-Encoding for nominal categorical values and Label Encoding for ordinal categorical values). After which we scaled our features to ensure that no single feature dominates the learning process due to its magnitude, afterwhich we carried on to modeling and evaluated our models using accuracy metrics.
After evaluating our multiple classification models; Random-Forest model performs quite well than Logistic Regression and Decision Tree models with an accuracy of 95.92%. This is due to its ensemble learning approach, where multiple decision trees are aggregated to reduce overfitting and improve generalization, making it more robust and accurate.
Random Forest handles complex, non-linear relationships and feature interactions better than Logistic Regression, which assumes linearity, and it is less prone to overfitting than a single Decision Tree. Although Decision Trees offer easy interpretability, they are more prone to overfitting and instability.
The Logistic Regression model achieved an accuracy of 83.68%, which is lower than both the Random Forest and Decision Tree models. Logistic Regression is a simple and interpretable model that works well when the relationship between the features and the target variable is linear. However, in cases like of our dataset which has complex, non-linear relationships, it struggles to capture the underlying patterns, leading to lower accuracy.
Overall, Random Forest is the best choice for this dataset, providing high accuracy and resilience to overfitting, Its ability to aggregate results from multiple trees reduces the model's variance, resulting in higher predictive performance.

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

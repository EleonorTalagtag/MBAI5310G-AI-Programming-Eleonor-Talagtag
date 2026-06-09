# Assignment 4: Decision Tree Models and Evaluation
## Business Overview and Problem
TalentWise Advisory is a mid-sized consulting and business services firm with teams in sales, customer support, operations, finance, marketing, IT, and human resources. The company delivers project-based services to corporate clients and depends heavily on skilled employees, client knowledge, and consistent team performance.

The main business problem is that managers often recognize employee attrition risk too late. By the time an employee resigns, the company has fewer options to address workload concerns, improve support, or offer career development opportunities.

•	Reduce preventable employee turnover and replacement costs.
•	Identify departments or employee groups with higher attrition risk.
•	Support employees earlier through coaching, workload review, training, or career discussions.
•	Improve workforce planning and reduce disruption to client projects.

## Files in This Folder
•	DecisionTree_EmployeeAttrition.ipynb
•	talentwise_employee_attrition_dataset.xlsx
•	Model Output
•	Business interpretation
  
## Dataset or Input Source
The dataset used in this project contains simulated hotel booking records for StayEase Boutique Hotels. Each row represents one reservation and includes booking behavior, customer history, trip details, and revenue-related information.
Some important features include:
•	Department
•	Role_Level
•	Employment_Type
•	Education_Level
•	Tenure_Months
•	Monthly_Salary
•	Overtime_Hours_Last_Month
•	Training_Hours_Last_Quarter
•	Performance_Rating
•	Engagement_Score
•	Manager_Support_Score
•	Remote_Work_Days_Per_Week
•	Absence_Days_Last_Quarter
•	Promotion_Last_Year
•	Commute_Distance_KM
•	Workload_Score
•	Salary_Satisfaction
The target variable is:
•	Left_Company 
  1 = Left/Resigned
  0 = Stayed

Note that Employee_ID was removed before training the model because it is only a unique identifier and does not provide meaningful information for predicting whether an employee will leave or stay with the company.

## Methods Used
This project uses a Decision Tree Classification model from Scikit-learn to predict whether an employee is likely to leave or stay with the company based on employee-related features.

Before training the model, the Employee_ID column was removed because it is only a unique identifier and does not contribute meaningful information for predicting employee attrition.

The dataset was divided into training and testing sets to evaluate model performance on unseen employee data. The model was then evaluated using classification metrics such as accuracy, precision, recall, F1-score, and confusion matrix analysis.

The Decision Tree model was configured with:
max_depth = 4
random_state = 42

## Main Evaluation Results
The Decision Tree model was evaluated using common classification metrics:
| Metric    | Score  |
| --------- | ------ |
| Accuracy  | 79.17% |
| Precision | 44.44% |
| Recall    | 28.57% |
| F1-Score  | 34.78% |

The Decision Tree model showed moderate performance in predicting employee attrition. The relatively high accuracy indicates that the model correctly classified many employee records overall, particularly employees who stayed with the company. However, the lower precision, recall, and F1-score show that the model still struggled to accurately identify employees who actually left the company.

Recall was considered especially important for this business problem because the company wants to identify employees at risk of leaving as early as possible. A higher recall would help managers provide earlier support, such as workload reviews, coaching, training opportunities, or career development discussions before employees resign.

The lower recall result also means that the model missed several actual attrition cases, so the model should be used as a decision-support tool rather than the only basis for HR decisions.

## Key Business Insights
The Decision Tree model helped identify employee characteristics associated with higher attrition risk. These insights can help TalentWise Advisory support employees earlier and improve workforce planning and retention strategies.

The model can support the business by:

Identifying employees who may be at higher risk of leaving
Helping HR managers prioritize retention and support efforts
Supporting workload reviews, coaching, training, and career development discussions
Improving workforce planning and reducing disruption to client projects
Understanding attrition patterns related to engagement, manager support, workload, overtime, and salary satisfaction

The model results also highlight the business impact of false predictions.

False positives occur when the model predicts that an employee will leave, but the employee actually stays. In this situation, HR teams may spend unnecessary time and resources on retention activities for employees who are not truly at risk of leaving.

False negatives occur when the model predicts that an employee will stay, but the employee actually leaves. This is especially important for this business problem because the company may fail to recognize attrition risk early enough to provide support or intervention before the employee resigns. This can lead to recruitment and training costs, project disruption, loss of experienced employees, and reduced productivity.

Overall, the model provides useful insights into employee attrition behavior that can help support more proactive and informed HR decision-making.

## One Limitation of the Model
The dataset is synthetic and may not fully represent real-world employee behavior or workplace situations. Important factors such as employee motivation, personal circumstances, workplace culture, economic conditions, and external job opportunities were not included in the dataset. These limitations may affect the model’s ability to accurately predict employee attrition in real business environments.

## Responsible AI Reflection
Although the Decision Tree model provided useful insights into employee attrition behavior, responsible and ethical use of the model is still important. The model produced several incorrect predictions, so it should be used only as a decision-support tool rather than the sole basis for HR decisions.

Some features, such as engagement scores, manager support, workload, and salary satisfaction, may unintentionally introduce bias if certain employee groups are overrepresented in the dataset. In addition, the dataset is synthetic and may not fully represent real-world workplace situations.

Human judgment is still necessary because managers may need to consider other important factors not included in the dataset, such as employee motivation, personal circumstances, workplace relationships, or external job opportunities. The company should also protect employee privacy and use the model fairly and transparently when supporting retention decisions.
  
## How to Run or Review
1. Save the talentwise_employee_attrition_dataset.xlsx file in the Jupyter Notebook root folder or working directory.
2. Open the DecisionTree_EmployeeAttrition.ipynb file using Jupyter Notebook or JupyterLab.
3. Run the notebook cells sequentially.

# Assignment 4: Decision Tree Models and Evaluation
## Business Overview and Problem
StayEase Boutique Hotels is a mid-sized hospitality company operating city, airport, and resort-style hotel properties. The company receives reservations through several channels, including its direct website, online travel agencies, corporate portals, travel agents, and phone reservations.

The main business challenge is booking cancellation. When a guest cancels close to the arrival date, the hotel may lose revenue because the room cannot always be resold. At the same time, if the hotel assumes too many guests will cancel, it may overbook rooms and create poor customer experiences.

The goal of this assignment is to help StayEase use historical booking data to predict whether a booking is likely to be cancelled. 

## Files in This Folder
•	DecisionTree_BookingCancellation.ipynb
•	stayease_hotel_booking_cancellation_dataset.xlsx
•	Model Results and Outputs
•	Business interpretation
  
## Dataset or Input Source
The dataset used in this project contains simulated hotel booking records for StayEase Boutique Hotels. Each row represents one reservation and includes booking behavior, customer history, trip details, and revenue-related information.
Some important features include:
•	Lead_Time_Days
•	Booking_Channel
•	Deposit_Type
•	Weekend_Nights
•	Weekday_Nights
•	Adults
•	Children
•	Previous_Cancellations
•	Repeated_Guest
•	Average_Daily_Rate
•	Meal_Plan
•	Parking_Requested
The target variable is:
•	Booking_Cancelled
  1 = Booking Cancelled
  0 = Booking Not Cancelled

## Methods Used
This project uses a Decision Tree Classification model from Scikit-learn. The model was trained to classify hotel bookings as either likely to be cancelled or likely to be completed.

The Decision Tree model was configured with:
•	max_depth = 4
•	random_state = 42

## Main Evaluation Results
The model was evaluated using common classification metrics:
Metric	Score
Accuracy	57.89%
Precision	42.86%
Recall	55.56%
F1-Score	48.39%

The Decision Tree model showed moderate performance in predicting hotel booking cancellations. The model was able to identify some cancellation patterns, but it still produced several incorrect predictions. Recall was considered especially important because the business wants to identify as many potential cancellations as possible before the arrival date. Detecting more possible cancellations early can help the hotel improve room planning, manage overbooking risks, and reduce possible revenue loss.

## Key Business Insights
The Decision Tree model can help StayEase Boutique Hotels identify booking patterns that may increase the likelihood of cancellation. By predicting potentially risky reservations before the guest arrival date, the hotel can improve operational planning and reduce possible revenue loss.

The model can support the business by:

Identifying high-risk bookings earlier
Sending reminder emails or confirmation requests to customers with higher cancellation risk
Improving room inventory management and overbooking decisions
Understanding cancellation trends across booking channels, deposit types, and customer booking behavior
Supporting better revenue management and operational planning

Important features such as lead time, booking channel, deposit type, rep
## Responsible AI Reflection
- Some features such as Age, Annual_Premium, Years_With_Company, Satisfaction_Score, Number_of_Claims, and Payment_Method may introduce possible bias in the prediction results if certain customer groups are underrepresented or overrepresented in the dataset. These features may unfairly favor or disadvantage some customers during prediction.
- The dataset contains customer-related information, so proper data privacy and security measures should be followed when handling, storing, and processing the data to protect sensitive customer information.
- False positives occur when the model predicts that a customer will renew their insurance policy, but the customer actually does not renew. False negatives occur when the model predicts that a customer will not renew their policy, but the customer actually renews it. These prediction errors may affect customer retention strategies, marketing decisions, and business planning.
- The dataset may not fully represent all customer characteristics or behaviors. Important factors such as financial capacity or income, the number of existing insurance policies, and a customer’s willingness to maintain multiple policies are not included in the dataset. These missing features may affect the fairness and accuracy of the model’s predictions.
- The model predictions should only be used as a reference to support business decisions and not as the sole basis for approving or denying customer actions. Human review is still recommended before applying the model in a real business environment to ensure fairness, accuracy, and responsible decision-making.
## How to Run or Review
1. Save the insurance_policy_renewal_dataset.xls file in the Jupyter Notebook root folder or working directory.
2. Open the Assignment3_Classification-Models-and-Evaluation.ipynb file using Jupyter Notebook or JupyterLab.
3. Run the notebook cells sequentially from top to bottom to execute the data preprocessing, model training, evaluation process and interpreting the result.

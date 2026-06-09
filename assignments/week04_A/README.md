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
The Decision Tree model helped identify booking characteristics associated with higher cancellation risk. These insights can support StayEase Boutique Hotels in making better operational and revenue management decisions before the guest arrival date.

The model can support the business by:
•	Identifying bookings with higher cancellation risk
•	Improving room allocation and overbooking decisions
•	Supporting proactive guest communication, such as reminder or confirmation emails
•	Analyzing cancellation behavior across booking channels and deposit types

The model results also highlight the business impact of false predictions. False positives occur when the model predicts that a booking will be cancelled even though the guest actually arrives. This may lead to unnecessary business actions, such as inaccurate overbooking decisions or unnecessary customer follow-ups. False negatives occur when the model predicts that a booking will not be cancelled, but the guest actually cancels. This may result in empty rooms, missed opportunities to resell reservations, and possible revenue loss.

Overall, the model provides useful insights into customer booking behavior that can help improve operational efficiency and support more informed business decision-making.

## One Limitation of the Model
One limitation of the model is that the dataset is simulated and may not fully represent real-world hotel booking behavior. Factors such as weather conditions, flight delays, emergencies, local events, and sudden travel restrictions are not included in the dataset. In addition, the model may learn patterns from historical business practices that could introduce bias into predictions.

## Responsible AI Reflection
Although the Decision Tree model provided useful insights into booking cancellation behavior, responsible and ethical use of the model is still important. The model achieved only moderate performance and produced several incorrect predictions, which means it should not be used as the sole basis for business decisions.

Some booking features, such as booking channel, deposit type, repeated guest status, and previous cancellations, may unintentionally introduce bias into predictions if certain customer groups are overrepresented or underrepresented in the dataset. In addition, the dataset is simulated and may not fully represent real-world booking behavior and customer situations.

The model should be used only as a decision-support tool to help hotel managers identify possible cancellation risks. Human judgment is still necessary because managers may need to consider other important factors that are not included in the dataset, such as weather conditions, emergencies, travel disruptions, or special customer situations.

The hotel should also ensure that customer booking information is handled responsibly by protecting data privacy and using the model fairly and transparently when supporting operational decisions.
  
## How to Run or Review
1. Save the stayease_hotel_booking_cancellation_dataset.xlsx file in the Jupyter Notebook root folder or working directory.
2. Open the DecisionTree_BookingCancellation.ipynb file using Jupyter Notebook or JupyterLab.
3. Run the notebook cells sequentially.

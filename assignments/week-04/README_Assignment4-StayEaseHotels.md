# Week [04] – [Assignment4: Decision Tree Model and Business Interpretation Based on a Business Plan]

## Task Overview - StayEase Boutique Hotels Business Plan for Booking Cancellation Predictions
-  Building a Decision Tree classification model and interpret the results from a business perspective.

## Task 1: Understand the Business Problem 
What is the business about?
-   The business is called StayEase Boutique Hotels. It is a hospitality company that offers resort-style hotel rooms within the city and near the airport. They offer bookings through many mediums including their website, online travel agencies, corporate portals, travel agents and through phone call. 
What problem is the business trying to solve?
- The are having a problem with booking cancellation. The hotel looses revenue when guests make last minute cancellations because they can not be booked on such short notice after cancellations. On the other hand, the hotel also struggles with overbooking because if some guests do not cancel and hotel becomes overbooked, it will result in unhappy customers. These cancellations affect revenue forecasting, staffing, inventory planning and customer service quality. 
What decision can machine learning help the business make?
- Machine learning can help the business make decisions by identifying the bookings that are likely to be cancelled and classifying bookings that are to be cancelled or to be completed. Receiving these predictions early on in the booking process can help to mitigate some of the issues faced by the business as a result of early cancellations. 
What is the target variable in the dataset?
- The target variable in this dataset is the booking being cancelled.
- Booking_Cancelled = 1
- Booking_NotCancelled = 0
What are the input features?
- Booking behaviour: Lead_Time_Days, Booking_Channel, Deposit_Type
- Customer history: Repeated_Guest, Previous_Cancellations, Loyalty_Points
- Trip details: Weekend_Nights, Weekday_Nights, Adults, Children, Room_Type
- Revenue information: Average_Daily_Rate, Meal_Plan, Parking_Requested
Why is this prediction useful for the business?
- This prediction will allow the business to make strategic decisions beforehand based on the amount of guests who are likely to cancel. They can identify high-risk bookings, adjust room availability, check if some bookings are at higher risks than others, improve loyalty for customers with lower risks and support revenue.

## Task 2: Prepare the Data 
Dataset Used: stayease_hotel_booking_cancellation_datatset
Dataset was downloaded as an .xls file and converted to a .csv file to be used on Jupyter Notebook for assignment 3.
The dataset contains information such as booking ID, customer type, hotel type, arrival month, booking channel, etc. 
Steps Completed: 
1. Load the dataset
2. Inspect the dataset
3. Check the number of rows and columns
4. Check data types
5. Check missing values
6. Check duplicate rows
7. Clean the dataset if needed
8. Separate features and target variable
9. Handle categorical and numerical variables if needed
10. Split the data into training and testing sets

## Task 3: Train a Decision Tree Classification Model
Machine-Learning Model Used: Decision Tree Classification Model

## Task 4: Business Interpretation of Model Results
How well did the Decision Tree model perform?
- The decision tree model performed moderately well given it has an accuracy of around 0.7. 
Is there a large difference between training accuracy and testing accuracy?
- Training accuracy: 0.71
- Testing accuracy: 0.69
- No, there is minimal difference between the two. 
Does the model show signs of overfitting? Why or why not?
- The model does not show signs of overfitting because the training and testing accuracy is almost the same value (very close in range, 0.02 difference)
Which evaluation metric is most important for this business problem?
- Recall is the most important evaluation metric in this case because we want to find the number of actual cancellations the model can identify. By doing so, the business can then identify the cancellations and implement preventative measures beforehand. 
What do false positives mean in this business context?
- A false positive would mean a booking that is shown as will be cancelled but will not actually be cancelled.
What do false negatives mean in this business context?
- A negative would mean a booking that is showing that it will not get cancelled but actually will get cancelled. 
Which features were most important in the Decision Tree model?
- The most important features were Average_Daily_Rate, Lead_Time_Days, and Special_Requests. 
How can these important features help the business make better decisions?
- These features can help the business make better decisions. For instance, Average_Daily_Rate can help the business understand if the pricing has any effect on the cancellation, Lead_Time_Days can show the business how many days leading up to the reservation the customer booked the hotel room, and finally Special_Requests can help the business understand any underlying/hidden aspects that could affect cancellations. 
What is one possible limitation or bias in the model or dataset?
- One of the possible limitations to this dataset is the small sample size. The data currenly shows 380 bookings which may not be an adequate number to fully represent cancellation predictions. 
Why should human judgment still be used when making business decisions based on model results?
- Human judgement should still be used when making decisions based on model results because some features or factors may require further interpretation. The business must take into account bias and specific personal attributes of customers. Other factors that should be considered include weather, flight disruption, local events, etc. 


First 5 Rows:
  Booking_ID Booking_Date              Hotel_Type Arrival_Month  \
0     BK0001   2026-02-10         Lakeside Resort      December   
1     BK0002   2026-02-28         Lakeside Resort          July   
2     BK0003   2026-02-28  Airport Business Hotel          June   
3     BK0004   2026-02-05    City Center Boutique      December   
4     BK0005   2026-01-01         Lakeside Resort      November   

        Booking_Channel Market_Segment   Customer_Type Reserved_Room_Type  \
0        Direct Website         Family  Loyalty Member           Standard   
1  Online Travel Agency        Leisure       New Guest           Standard   
2     Phone Reservation     Conference       New Guest              Suite   
3          Travel Agent       Business       New Guest           Standard   
4  Online Travel Agency         Family       New Guest              Suite   

            Meal_Plan     Deposit_Type  ...  Adults  Children  \
0           Room Only       No Deposit  ...       2         0   
1           Room Only  Partial Deposit  ...       2         0   
2  Breakfast Included       No Deposit  ...       2         0   
3  Breakfast Included   Non-refundable  ...       3         0   
4           Room Only       No Deposit  ...       3         0   

   Previous_Cancellations  Repeated_Guest  Special_Requests  \
0                       0               1                 1   
1                       3               0                 1   
2                       0               0                 0   
3                       0               0                 1   
4                       0               0                 1   

   Average_Daily_Rate  Parking_Requested  Loyalty_Points  Booking_Cancelled  \
0              218.04                 No            1599                  0   
1              248.94                Yes               0                  1   
2              418.14                 No               0                  0   
3              180.31                 No               0                  0   
4              306.34                 No              43                  1   

  Unnamed: 22  
0         NaN  
1         NaN  
2         NaN  
3         NaN  
4         NaN  

[5 rows x 23 columns]

Dataset Information:
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 380 entries, 0 to 379
Data columns (total 23 columns):
 #   Column                  Non-Null Count  Dtype  
---  ------                  --------------  -----  
 0   Booking_ID              380 non-null    object 
 1   Booking_Date            380 non-null    object 
 2   Hotel_Type              380 non-null    object 
 3   Arrival_Month           380 non-null    object 
 4   Booking_Channel         380 non-null    object 
 5   Market_Segment          380 non-null    object 
 6   Customer_Type           380 non-null    object 
 7   Reserved_Room_Type      380 non-null    object 
 8   Meal_Plan               380 non-null    object 
 9   Deposit_Type            380 non-null    object 
 10  Lead_Time_Days          380 non-null    int64  
 11  Weekend_Nights          380 non-null    int64  
 12  Weekday_Nights          380 non-null    int64  
 13  Adults                  380 non-null    int64  
 14  Children                380 non-null    int64  
 15  Previous_Cancellations  380 non-null    int64  
 16  Repeated_Guest          380 non-null    int64  
 17  Special_Requests        380 non-null    int64  
 18  Average_Daily_Rate      380 non-null    float64
 19  Parking_Requested       380 non-null    object 
 20  Loyalty_Points          380 non-null    int64  
 21  Booking_Cancelled       380 non-null    int64  
 22  Unnamed: 22             0 non-null      float64
dtypes: float64(2), int64(10), object(11)
memory usage: 68.4+ KB
None

Statistical Summary:
       Lead_Time_Days  Weekend_Nights  Weekday_Nights      Adults    Children  \
count      380.000000      380.000000      380.000000  380.000000  380.000000   
mean        64.184211        1.023684        3.102632    1.897368    0.481579   
std         37.531169        0.942666        1.696650    0.773911    0.839134   
min          1.000000        0.000000        1.000000    1.000000    0.000000   
25%         37.000000        0.000000        2.000000    1.000000    0.000000   
50%         60.000000        1.000000        3.000000    2.000000    0.000000   
75%         89.000000        2.000000        4.000000    2.000000    1.000000   
max        183.000000        3.000000        7.000000    4.000000    3.000000   

       Previous_Cancellations  Repeated_Guest  Special_Requests  \
count              380.000000      380.000000        380.000000   
mean                 0.331579        0.589474          0.918421   
std                  0.812535        0.492578          0.956123   
min                  0.000000        0.000000          0.000000   
25%                  0.000000        0.000000          0.000000   
50%                  0.000000        1.000000          1.000000   
75%                  0.000000        1.000000          1.000000   
max                  4.000000        1.000000          4.000000   

       Average_Daily_Rate  Loyalty_Points  Booking_Cancelled  Unnamed: 22  
count          380.000000      380.000000         380.000000          0.0  
mean           206.636789     1688.276316           0.357895          NaN  
std             61.045068     1856.431949           0.480013          NaN  
min             85.000000        0.000000           0.000000          NaN  
25%            165.335000      150.500000           0.000000          NaN  
50%            200.250000      789.500000           0.000000          NaN  
75%            241.322500     2959.250000           1.000000          NaN  
max            418.140000     7332.000000           1.000000          NaN  

Rows and Columns:
(380, 23)
Number of Rows: 380
Number of Columns: 23

Data Types:
Booking_ID                 object
Booking_Date               object
Hotel_Type                 object
Arrival_Month              object
Booking_Channel            object
Market_Segment             object
Customer_Type              object
Reserved_Room_Type         object
Meal_Plan                  object
Deposit_Type               object
Lead_Time_Days              int64
Weekend_Nights              int64
Weekday_Nights              int64
Adults                      int64
Children                    int64
Previous_Cancellations      int64
Repeated_Guest              int64
Special_Requests            int64
Average_Daily_Rate        float64
Parking_Requested          object
Loyalty_Points              int64
Booking_Cancelled           int64
Unnamed: 22               float64
dtype: object

Missing Values:
Booking_ID                  0
Booking_Date                0
Hotel_Type                  0
Arrival_Month               0
Booking_Channel             0
Market_Segment              0
Customer_Type               0
Reserved_Room_Type          0
Meal_Plan                   0
Deposit_Type                0
Lead_Time_Days              0
Weekend_Nights              0
Weekday_Nights              0
Adults                      0
Children                    0
Previous_Cancellations      0
Repeated_Guest              0
Special_Requests            0
Average_Daily_Rate          0
Parking_Requested           0
Loyalty_Points              0
Booking_Cancelled           0
Unnamed: 22               380
dtype: int64

Duplicate Rows:
0
  Booking_ID Booking_Date              Hotel_Type Arrival_Month  \
0     BK0001   2026-02-10         Lakeside Resort      December   
1     BK0002   2026-02-28         Lakeside Resort          July   
2     BK0003   2026-02-28  Airport Business Hotel          June   
3     BK0004   2026-02-05    City Center Boutique      December   
4     BK0005   2026-01-01         Lakeside Resort      November   

        Booking_Channel Market_Segment   Customer_Type Reserved_Room_Type  \
0        Direct Website         Family  Loyalty Member           Standard   
1  Online Travel Agency        Leisure       New Guest           Standard   
2     Phone Reservation     Conference       New Guest              Suite   
3          Travel Agent       Business       New Guest           Standard   
4  Online Travel Agency         Family       New Guest              Suite   

            Meal_Plan     Deposit_Type  ...  Weekday_Nights  Adults  Children  \
0           Room Only       No Deposit  ...               2       2         0   
1           Room Only  Partial Deposit  ...               5       2         0   
2  Breakfast Included       No Deposit  ...               4       2         0   
3  Breakfast Included   Non-refundable  ...               2       3         0   
4           Room Only       No Deposit  ...               7       3         0   

   Previous_Cancellations  Repeated_Guest  Special_Requests  \
0                       0               1                 1   
1                       3               0                 1   
2                       0               0                 0   
3                       0               0                 1   
4                       0               0                 1   

   Average_Daily_Rate  Parking_Requested  Loyalty_Points Booking_Cancelled  
0              218.04                 No            1599                 0  
1              248.94                Yes               0                 1  
2              418.14                 No               0                 0  
3              180.31                 No               0                 0  
4              306.34                 No              43                 1  

[5 rows x 22 columns]
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 380 entries, 0 to 379
Data columns (total 22 columns):
 #   Column                  Non-Null Count  Dtype  
---  ------                  --------------  -----  
 0   Booking_ID              380 non-null    object 
 1   Booking_Date            380 non-null    object 
 2   Hotel_Type              380 non-null    object 
 3   Arrival_Month           380 non-null    object 
 4   Booking_Channel         380 non-null    object 
 5   Market_Segment          380 non-null    object 
 6   Customer_Type           380 non-null    object 
 7   Reserved_Room_Type      380 non-null    object 
 8   Meal_Plan               380 non-null    object 
 9   Deposit_Type            380 non-null    object 
 10  Lead_Time_Days          380 non-null    int64  
 11  Weekend_Nights          380 non-null    int64  
 12  Weekday_Nights          380 non-null    int64  
 13  Adults                  380 non-null    int64  
 14  Children                380 non-null    int64  
 15  Previous_Cancellations  380 non-null    int64  
 16  Repeated_Guest          380 non-null    int64  
 17  Special_Requests        380 non-null    int64  
 18  Average_Daily_Rate      380 non-null    float64
 19  Parking_Requested       380 non-null    object 
 20  Loyalty_Points          380 non-null    int64  
 21  Booking_Cancelled       380 non-null    int64  
dtypes: float64(1), int64(10), object(11)
memory usage: 65.4+ KB
None

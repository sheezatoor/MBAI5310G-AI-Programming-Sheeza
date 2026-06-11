First 5 Rows:
  Customer_ID Campaign_Date  Age Annual_Income Customer_Segment  \
0   CUST-0001    2026-04-14   36       $58,196              New   
1   CUST-0002    2026-04-24   38       $49,043        Returning   
2   CUST-0003    2026-02-01   21       $45,952              New   
3   CUST-0004    2026-02-28   18      $107,638            Loyal   
4   CUST-0005    2026-03-01   50       $89,969        Returning   

             Region Campaign_Channel    Campaign_Type  Ad_Exposure_Count  \
0  British Columbia            Email  Brand Awareness                  4   
1           Ontario            Email      Retargeting                  5   
2           Ontario            Email   Discount Offer                  4   
3  British Columbia       Search Ads      Retargeting                  4   
4            Quebec       Search Ads      New Product                  1   

  Email_Opened  ... Previous_Purchases  Average_Order_Value  \
0          Yes  ...                  1              $131.51   
1          Yes  ...                  5               $27.61   
2          Yes  ...                  0              $104.65   
3          Yes  ...                 12              $135.31   
4          Yes  ...                  4               $27.49   

   Discount_Offered_Percent Days_Since_Last_Purchase  Loyalty_Score  \
0                        20                       60             54   
1                        20                       73             80   
2                        25                       39             14   
3                        20                       32             73   
4                         5                        5             40   

   Customer_Satisfaction  Social_Media_Engagement_Score  \
0                    5.0                             37   
1                    8.0                             50   
2                    8.0                             55   
3                    7.0                             23   
4                    7.0                             45   

   Prior_Campaign_Response  Converted Unnamed: 21  
0                       No         No         NaN  
1                       No         No         NaN  
2                       No        Yes         NaN  
3                       No        Yes         NaN  
4                       No         No         NaN  

[5 rows x 22 columns]

Dataset Information:
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 605 entries, 0 to 604
Data columns (total 22 columns):
 #   Column                         Non-Null Count  Dtype  
---  ------                         --------------  -----  
 0   Customer_ID                    605 non-null    object 
 1   Campaign_Date                  605 non-null    object 
 2   Age                            605 non-null    int64  
 3   Annual_Income                  595 non-null    object 
 4   Customer_Segment               599 non-null    object 
 5   Region                         605 non-null    object 
 6   Campaign_Channel               605 non-null    object 
 7   Campaign_Type                  605 non-null    object 
 8   Ad_Exposure_Count              605 non-null    int64  
 9   Email_Opened                   605 non-null    object 
 10  Ad_Clicked                     605 non-null    object 
 11  Website_Visits_Last_30_Days    605 non-null    int64  
 12  Previous_Purchases             605 non-null    int64  
 13  Average_Order_Value            599 non-null    object 
 14  Discount_Offered_Percent       605 non-null    int64  
 15  Days_Since_Last_Purchase       605 non-null    int64  
 16  Loyalty_Score                  605 non-null    int64  
 17  Customer_Satisfaction          597 non-null    float64
 18  Social_Media_Engagement_Score  605 non-null    int64  
 19  Prior_Campaign_Response        605 non-null    object 
 20  Converted                      605 non-null    object 
 21  Unnamed: 21                    0 non-null      float64
dtypes: float64(2), int64(8), object(12)
memory usage: 104.1+ KB
None

Statistical Summary:
              Age  Ad_Exposure_Count  Website_Visits_Last_30_Days  \
count  605.000000         605.000000                   605.000000   
mean    37.719008           3.600000                     6.185124   
std     11.254744           1.746899                     3.875818   
min     18.000000           1.000000                     0.000000   
25%     29.000000           2.000000                     3.000000   
50%     37.000000           4.000000                     6.000000   
75%     46.000000           5.000000                     8.000000   
max     70.000000           9.000000                    19.000000   

       Previous_Purchases  Discount_Offered_Percent  Days_Since_Last_Purchase  \
count          605.000000                605.000000                605.000000   
mean             3.370248                 17.438017                 48.009917   
std              3.052267                  8.986646                 33.345322   
min              0.000000                  0.000000                  1.000000   
25%              1.000000                 10.000000                 22.000000   
50%              3.000000                 20.000000                 44.000000   
75%              5.000000                 25.000000                 68.000000   
max             15.000000                 30.000000                164.000000   

       Loyalty_Score  Customer_Satisfaction  Social_Media_Engagement_Score  \
count     605.000000             597.000000                     605.000000   
mean       50.598347               6.482412                      45.218182   
std        22.964247               1.504504                      23.388074   
min         0.000000               2.000000                       0.000000   
25%        34.000000               5.000000                      29.000000   
50%        48.000000               7.000000                      45.000000   
75%        67.000000               7.000000                      61.000000   
max       100.000000              10.000000                     100.000000   

       Unnamed: 21  
count          0.0  
mean           NaN  
std            NaN  
min            NaN  
25%            NaN  
50%            NaN  
75%            NaN  
max            NaN  

Rows and Columns:
(605, 22)
Number of Rows: 605
Number of Columns: 22

Data Types:
Customer_ID                       object
Campaign_Date                     object
Age                                int64
Annual_Income                     object
Customer_Segment                  object
Region                            object
Campaign_Channel                  object
Campaign_Type                     object
Ad_Exposure_Count                  int64
Email_Opened                      object
Ad_Clicked                        object
Website_Visits_Last_30_Days        int64
Previous_Purchases                 int64
Average_Order_Value               object
Discount_Offered_Percent           int64
Days_Since_Last_Purchase           int64
Loyalty_Score                      int64
Customer_Satisfaction            float64
Social_Media_Engagement_Score      int64
Prior_Campaign_Response           object
Converted                         object
Unnamed: 21                      float64
dtype: object
DecisionTreeClassifier(max_depth=5, random_state=42)

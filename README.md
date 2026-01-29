# Tuoc-Nguyen-Projects
Data Overview : 

The Supermarket Sale dataset captures granular transaction-level data from a retail supermarket chain with operations spanning multiple branches and cities. Each record corresponds to a single purchase and documents key details including the store branch and city, customer segment, product and category, quantity sold, and the total transaction value in USD.

According to my Macbook limitation related to Excel function, I use Python and Excel to solve these homework tasks. 

Data cleaning :

First, I upload the xlsx file to google collab. After that, I use function df.info() to check whether there is any missing value
    
     <img width="533" height="153" alt="image" src="https://github.com/user-attachments/assets/1fa8e147-5a65-4ade-8d94-f4be65f33eea" />



 

After that, I use function df.info() in my case is supermarket_sale.info() to check whether there is any missing value. And the result there are 3 categories have missing value which are : 
-	Customer type : 3 missing values (250 compared to 253) 
-	Product category :  6 missing values (247 compared to 253)
-	Quantity: 3 missing values (250 compared to 253)


 
To double check, I use function  supermarket_sale.isna().sum() to Return the number of missing values by column. 

 

I will eliminate all the missing values by using dropna() method without any data cooking. The result returns 242 results   

Otherwise, I can use quantity means to replace missing values in the quantity section by using fillna() method. This method aim to imputing new values into N/a values. Anotherway to solve this problem is leave it alone.

 
Similarly, I can use the function iloc() to update specific values in the product category section. In this case, I use this method to change product categories and customer types. However, as I mentioned above, I will remove values which are missing to maintain the authenticity of the report. After finishing, I import the excel.
 



Descriptive analysis:

After processing data, I use Descriptive Statistic function to find out the insight of Quantity and Total price categories

 

And the result: 





 

The results show that customers purchased an average of 10.77 items per transaction, with most buying between 10 and 11 items, indicating a relatively consistent shopping pattern. The average total spending per transaction was $126.57. Still, the large standard deviation of 102.93 and the maximum of $424.96 reveal substantial variation in spending behavior. At the same time, most customers make moderate purchases, a small group of high-spending customers considerably raises total revenue. This suggests an opportunity for the business to identify and engage these premium buyers to increase profitability, while still maintaining the stable base of regular shoppers.

 
 

Customer type	Count of quantity
Member	127
Normal	115
Grand Total	242

Member customers recorded 127 transactions, slightly exceeding the 115 transactions made by normal customers, which indicates a higher frequency of repeat visits among members. This pattern suggests that the membership program is contributing positively to customer loyalty and sustained engagement. As a result, the company should continue to encourage membership sign-ups and enhance loyalty benefits, such as point-based reward schemes, to further improve customer retention.

 


Product categories	Count of quantity
Beverages	47
Fruits	58
Household	54
Personal Care	39
Stationery	44
Grand Total	242

The chart indicates that Fruits and Household items account for the largest share of transactions, highlighting their role as regularly purchased essentials. In contrast, Personal Care and Stationery record fewer transactions, reflecting lower purchase frequency. This insight suggests that managers should prioritize inventory availability for high-demand categories, while applying targeted promotions or incentives to stimulate demand in categories with lower transaction volumes.

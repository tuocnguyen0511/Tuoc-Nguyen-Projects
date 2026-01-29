# MIS 311 - Portfolio Project :

Dataset: Supermarket Sale

Student: Nguyen Trong Tuoc

IRR: 2432300332



**Data Overview :** 

The Supermarket Sale dataset captures granular transaction-level data from a retail supermarket chain with operations spanning multiple branches and cities. Each record corresponds to a single purchase and documents key details including the store branch and city, customer segment, product and category, quantity sold, and the total transaction value in USD.

According to my Macbook limitation related to Excel function, I use Python and Excel to solve these homework tasks. 

**Data cleaning :**

First, I upload the xlsx file to google collab. After that, I use function df.info() to check whether there is any missing value
<img width="533" height="153" alt="image" src="https://github.com/user-attachments/assets/45f57ab7-3c01-4498-b84d-44a592895f5c" />






 

After that, I use function df.info() in my case is supermarket_sale.info() to check whether there is any missing value. And the result there are 3 categories have missing value which are : 
-	Customer type : 3 missing values (250 compared to 253) 
-	Product category :  6 missing values (247 compared to 253)
-	Quantity: 3 missing values (250 compared to 253)
  <img width="491" height="274" alt="image" src="https://github.com/user-attachments/assets/fadb9c7e-6315-4ffd-9eae-299b4575381c" />

  



 
To double check, I use function  supermarket_sale.isna().sum() to Return the number of missing values by column. 


<img width="145" height="152" alt="image" src="https://github.com/user-attachments/assets/c5e587fe-3421-44f6-9eb5-22e8dfd8223f" />


 

I will eliminate all the missing values by using dropna() method without any data cooking. The result returns 242 results   
<img width="698" height="239" alt="image" src="https://github.com/user-attachments/assets/7aaf3028-8b15-4356-8dcf-c4963582eb3e" />


Otherwise, I can use quantity means to replace missing values in the quantity section by using fillna() method. This method aim to imputing new values into N/a values. Anotherway to solve this problem is leave it alone.
<img width="634" height="128" alt="image" src="https://github.com/user-attachments/assets/e54d373a-7e2c-4915-8321-edf6f512e5fe" />




 
Similarly, I can use the function iloc() to update specific values in the product category section. In this case, I use this method to change product categories and customer types. However, as I mentioned above, I will remove values which are missing to maintain the authenticity of the report. After finishing, I import the result to excel file. 


 <img width="539" height="204" alt="image" src="https://github.com/user-attachments/assets/67d9590e-68b0-4e19-aed2-348f213f3510" />



 




**Descriptive analysis:**

After processing data, I use Descriptive Statistic function to find out the insight of Quantity and Total price categories
    
<img width="518" height="337" alt="image" src="https://github.com/user-attachments/assets/55896a06-c4f1-4ee7-9245-50b7a6c01bb4" />








 

And the result: 


<img width="205" height="174" alt="image" src="https://github.com/user-attachments/assets/fb4a4f6e-b682-4066-be89-78f3f417ef99" />











 

The results show that customers purchased an average of 10.77 items per transaction, with most buying between 10 and 11 items, indicating a relatively consistent shopping pattern. The average total spending per transaction was $126.57. Still, the large standard deviation of 102.93 and the maximum of $424.96 reveal substantial variation in spending behavior. At the same time, most customers make moderate purchases, a small group of high-spending customers considerably raises total revenue. This suggests an opportunity for the business to identify and engage these premium buyers to increase profitability, while still maintaining the stable base of regular shoppers.


<img width="357" height="214" alt="image" src="https://github.com/user-attachments/assets/2c2c2cab-7910-4b99-a679-4d8cbeb1f708" />


**Chart 1: Number of transaction by customer**
 


 

Customer type	Count of quantity
Member	127
Normal	115
Grand Total	242

Member customers recorded 127 transactions, slightly exceeding the 115 transactions made by normal customers, which indicates a higher frequency of repeat visits among members. This pattern suggests that the membership program is contributing positively to customer loyalty and sustained engagement. As a result, the company should continue to encourage membership sign-ups and enhance loyalty benefits, such as point-based reward schemes, to further improve customer retention.

**Chart 2: Number of transaction by Product Category**

 <img width="322" height="193" alt="image" src="https://github.com/user-attachments/assets/c88ebe47-3728-4963-bebb-a5d613fde877" />






Product categories	Count of quantity
Beverages	47
Fruits	58
Household	54
Personal Care	39
Stationery	44
Grand Total	242

The chart indicates that Fruits and Household items account for the largest share of transactions, highlighting their role as regularly purchased essentials. In contrast, Personal Care and Stationery record fewer transactions, reflecting lower purchase frequency. This insight suggests that managers should prioritize inventory availability for high-demand categories, while applying targeted promotions or incentives to stimulate demand in categories with lower transaction volumes.

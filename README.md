# Marketing Analysis Report For National Clothing Company

## Overview 

This is Udacity’s third and final project under the Nanodegree Program Data Analysis and Visualization with Microsoft Power BI and focuses on advanced data analysis. (Completed on November 9, 2023) 

For our third project, we have been tasked on helping a fictional online national clothing chain with creating a targeted marketing campaign. Sales have been flat and they want to lure lost customers back. The goal is to advertise specific products to specific customers in specific locations, but they don’t know who to target. 

## Sources 

US Census Bureau 

- Average income 

- location 

- population 

- industry 

Business Data 

- Product inventory 

- Product prices 

- Customer rating 

- Product return rate 

Customer Data 

- Customer ID 

- Names 

- Location 

- Date of birth 

- Purchase history 

Additional Data 

- Weather 

 
## Project Instructions 

In this project, we used population statistics from the US Census Bureau to determine where the greatest income exists around the country and whether there is a correlation between sales and income. We don’t know the incomes of our customers, but we should be able to predict it by looking at their purchase history and locations and comparing that against the census data. Additionally, we want to analyze our inventory, specifically customer ratings and return rate and see if there’s a correlation between the two. 

## Analysis Questions 

1. What is the correlation (R2 value) between sales and income? 

2. What is the correlation (R2 value) between customer ratings and product return rate? 

3. What are the linear regression formulas to predict customer income from customer sales? 

4. Which customer do you predict has the highest income? 

5. Which product will be advertised the most? 

 ## Sources 

The source material for this project can be found under the folder called “source files”.  

- Average Temperatures by State 

- Census Data 

- Customer List 

- Purchase List 

- State List 


## ETL 

- Used Power Query to split the columns under the Product Inventory table using the Delimiter function. Further data transformation were needed such as changing data type, promoting header, and merging columns. 

- For the Purchase List table, I used Power Query’s unpivot function to unpivot the multiple-date  columns as well as updating data types and renaming columns 

 
## Data Model 

![DataModel](https://github.com/cooljade007/MarketingAnalysisReportForNationalClothingCompany/assets/42302130/729dda77-3196-4332-b5d6-90701ba3f9fd)

## Analysis and Visualization 

The report consists of the following pages: 

- Overview 

- Predicted Income 

- Products 

- Customers 

#### Overview 

![Overview](https://github.com/cooljade007/MarketingAnalysisReportForNationalClothingCompany/assets/42302130/4acaa444-b708-4e46-a920-32874bb7fbfc)
 
#### Predicted Income Summary 

![Predicted Income](https://github.com/cooljade007/MarketingAnalysisReportForNationalClothingCompany/assets/42302130/621d7c88-483d-4293-bbe6-15ef805093e4)

- Using each state’s average Income and each state’s average Last 6 Months of Purchase, we used Linear Regression to predict an individual customer’s income. 

- There is a pretty strong positive correlation of .78 between the Average Income and the Average Last 6 Months of Purchases.  

- The linear regression formula is Y = .01X + -722.14. 

  - X represents the Predicted Income 

  - Y represents the Last 6 Months of Purchases 

#### Product Summary 

![Products](https://github.com/cooljade007/MarketingAnalysisReportForNationalClothingCompany/assets/42302130/d43ff446-698c-4ae9-b7ca-7ab2be82e5eb)

- There is a strong negative correlation of .69 between the Customer Rating and the Return Rate.  

- I thought it would be useful to grab each state’s temperature data since some of our products we offer are dependent on how cold or how hot it is outside. Hottest States are based on each state’s Average Highest Temperature and the Coldest States are based on each state’s Average Lowest Temperature. 

  - Floria and Hawaii are considered one of the hottest states meanwhile Alaska and Wyoming are considered one of the coldest states. 

- A few of the best products with highest Customer Rating and lowest Return Rate is the Chronograph Watch, Long Dress, and Leather Steakers. All of these products are not for any specific weather and are considered to be of medium cost as compared to the other products we sale. 

- We have a very large inventory value for Leather Bags. Leather Bags are our most expensive product we offer but has a pretty high return rate and low customer rating. 

- Winter gloves has the highest return rate and one of the lowest customer ratings. 

#### Customer Summary 

![Customer](https://github.com/cooljade007/MarketingAnalysisReportForNationalClothingCompany/assets/42302130/96b95946-4dcc-44ab-a593-a7cde82c4f98)

- We predict customer Jon Little to have the highest income of $556,790.49.  

- Customers tend to spend more during the months of September and December. 

- Most of the customers fall under the age group of 35 to 44 years old. 

- A large majority of our customers are from California and Florida. 
 

#### Recommendation 

The 3 products we are focusing on are Leather Bags, Sweaters, and Shirts. 

- Leather Bags are the most expensive product we offer and due to the cost, we should focus our marketing to states with the highest average predicted incomes, which is California and Florida. Since we can wear leather bags anytime of the year, we do not have to consider the weather. Customers in these states tend to spend more during the months of September and December so it would be advisable to focus our marketing efforts during those months. Based on our data from our customer rating and return rate, we should also focus on improving the quality of our Leather Bags. Leather Bags has one of the lowest Customer Rating and a somewhat medium Return Rate. We should also look into more on why customers are not satisfied with this product in order to improve our sales. 

- We offer 2 types of sweaters: Sweater Dress and Cotton Sweater. Since sweaters are for colder weather, we should look to focus our marketing of these products in states like Alaska, Wyoming, North Dakota, Montana, and Minnesota. Since Sweater Dresses are above average in cost, we should also focus on customers who have above average predicted income. 

- We offer a variety of different shirts and are considered one of the cheaper products we sale. Since customers can wear shirts anytime of the year, we don’t really need to consider the weather. Our shirts have pretty decent customer ratings. I recommend we market these products to all of our customers.  

- Other Products: 

  - We should also focus our marketing on our 3 highest rated products: Long Dress, Leather Sneakers, and Chronograph Watch. All 3 of these products also have one of the lowest return rate in our inventory. These 3 products can be worn anytime of the year so we do not have to consider the state’s weather. 

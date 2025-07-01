## AMAZON E-COMMERCE SALES ANALYSIS
   
### THE PROJECT TOPIC: REVIEW ANALYSIS OF AMAZON PRODUCT
Amazon product review analysis project of the Digital Skillup Africa (DSA) was given to me as a Junior Data Analyst. It is part of the prerequisit assignment that will inturn help me to up-skill my career and be rated as a data analyst. 

### PROJECT OVERVIEW:
Amazon is a company that provides E-commerce sales. They deals with different kinds of equipment/electronics and gadgets ranging from electronicsa and  accessorys, computer/accessories, car and motor bikes accessories, helath and personal care medical equipments, musical instrument, office products, toys and games etc. This data anlysis project allows to generate insight that can gide product improvement,marketing strategies and customer engagement of the company

### DATA SOURCE:
Amazon Sales Data: The primary dataset used for this analysis is the "Amazon_Case_Study.xlsx" file. The dataset contains information from each sales which includes;
* Product details: name, category, price, discount and ratings
* Customer engagement: user reviews, titles, an content

### TOOLS USED: 
- Microsoft Excel (https://www.microsoft.com), other tools I used to explore are;
- Excel Power query (for cleaning of the data)
- Calculated columns (for creating new metrics of KPIs)
- Pivot Charts( for visualizing of the summarized data
- Pivot tables (to analyze the data from different angles to identify trends and patterns so as to make informed decision.

###  The EXPLORATORY DATA ANALYSIS (EDA):
A Comprehensive Exploratory Data (EDA) were deployed using Excel tools and relevant techniques to the context of each analysis. I will explore the Amazon sales data to answer these keys questions. 
##### Task Question 1:
* The analysis will be based on the use of Pivot tables and calculated columns where necessary to answer the following;
  1. Find the average discount percentages by Product category
  2. Check how many products that are listed under each category
  3. Calculate the total number of review per category
  4. show product that has the highest average ratings
  5. acertain the average actual prices Vs the discounted prices by category
  6. List the products that have the highest number of reveiws
  7. Find how  many products that have a discount of 50% or more
  8. Show the distribution of product ratings i.e. how many products that are rateed 3.0, 4.0 etc
  9. calculate thetotal potential revenue of actual price * rating count by category
  10. Finds out the number of unique products per price range bucket e.g. <200, <200-500, >500
  11. To Know How the rating relate to the level of discount
  12. Check how many products have fewer than 1,000 reviews
  13. Which categories have product with teh hest discounts
  14. To identify the top 5 products in terms of rating and number of reviews combined
  
#### Task Question 2: Dashboard Creation
I will use the clean dataset and pivot outputs and build an Excel dashboard to unleash beautiful creativity

### DATA CLEANING/PREPARATION (EXCEL)
In view of the preparation task concerning this product, I performed the followings: we have 2 options for the cleaning. We can go by writing formular or use Excel power query, I choosed Power query instead. 
1. To "DATA" menu, from get and transform data, the table/range,
2. The data was loaded to the Excel power querry,
3. I viewed it to see the column quality, going through it, I observed that there was 1 error in rating count only. as far as am concerned the data is dirty.
4. I shortened the "category" aspected of the dataset to make it look good if not, in course of the analysis it may be too long.
5. Highlit and Right click on the category to choose split column by delimiter i.e. "left most delimiter", Okay, it split it into two, in the computer and accessories writing together
6. right click again to replace values i.e value to find & then replace with space (it will be divided into two
7. HomeImprovement, MusicalIstrument and Officepractice are still together and they are the three arguments I added space
8. Go to add column, "Conditional column", HomeImprovement, category 1, then HomeImprovement writing in space e.g. replace Home Improvement
9. add clause to repeat the remaining two i.e. MusicalInstrument and OfficePractice, Else Category 1
10. In the product name, count the number of character, I counted and stoped at 25 character including the spaces,
11. split the column again BUT not by delimiter, Split by number of character "once as far left as posible"
12. add the 25 and check on "once as far left as possible
13. Right Click and remove the splited right column
14. change the data types
15. I removed other columns that are not needed. the img link, user-name, review content and product link were removed because they are not necessary.
16. Close and Load my query.

#### Steps taken in Data Cleaning: Here are some interesting codes used in the course of this Cleaning analysis
- conditional columns
- split columns. See below the other codes; 

<img width="858" alt="Excel Power query" src="https://github.com/user-attachments/assets/e39c8e85-e74d-4e2e-bb75-ded5babd9126" />


#### Some writing calculated Column formulars: 
...xlsx

   To shortened the Product Category:
   =IFERROR(LEFT(C2,FIND("&",C2)-1)C2)

   To calculate the Potential Revenue:
   =Sum(actual price * Rating count)

   For Price Range:
   = IF(actual price <200, "<200",IF(actual price<=500,"200-500",">500"))

   For More than 50% Discount:
   =IF(H2>=50%,">50%","<50%")
   
### KEY METRICS

**POTENTIAL REVENUE:**

Having Calculated and sumed the Revenue by Product categories, as the power pivot tips  results indicates, 
   
<img width="273" alt="Potential Revenue" src="https://github.com/user-attachments/assets/bab84bd8-2e2b-4e02-890f-9e2d88d2e0d3" />

### INFERENCES:

There is a strong market demand of elecronics accessories, computer and accessories and Home kitchen accessories among the target audience. This could be because the pricing strategies is okay with the customers OR that the reviews might be driving sales. Also, the products has a competitive adavantage of unique values proposition/ features. This is evedenced in High Revenue generated of Electronics accessories: 91323,918,321, Computer Accessories: 11,628,224,483 and Home & Kitchen Accessories 10,459,722,337 respectively. Amazon Basics High-Speed Product(Product name) remains the product that has the highest number of reveiw as evidenced in sum of rating count of 853,946.00, BoAt Bassheads 100 in ear 772,426.00 and RedMi 9A Phone has 627,668.00 rating count. The company should tailor marketing strategies to the high revenue product categories with high revenue products 

On This Other hand, There is a Low revenue generation in Toys & Games, Car & motor bike, home improvement Health & personal care equipments. The inference might be because in the Categories, there is low demand from the audience or that the pricing straegy are not competitive. This inference is informed from the #2,380,050, #4,472,000, #6,163,434 and #6,959,700 revenue generated from the product categories. The company should monitor customer feedback and market trends to drive sales grwoth and product success of this goods also revise the procing, marketing or pricing from positioning from there, what is not working might start working.

**SLICER/FILTERING**


<img width="351" alt="REAL TIME FILTERING2" src="https://github.com/user-attachments/assets/8589245e-ca19-4136-bd07-c059b4c628ca" />


**Real-time filtering across(Slicer) Product category, Price Range Buckect and High Discount**


<img width="335" alt="Slicers " src="https://github.com/user-attachments/assets/c0c5cd4e-3a9a-42ef-862a-a61a79d0bfe9" />

### Creation of Dashboard Using the Cleaned Dataset and Pivot Outputs




<img width="427" alt="DashBoard Creation" src="https://github.com/user-attachments/assets/dd72ea8d-74d4-4160-b287-ae73b5a7a408" />

This DashBoard unleashed different creativity indicating a guide for data-driven decisions on marketing, resource allocation, pricing, most especially to derive sales growth and product features.

### RESULTS/FINDINGS:
   The result of the analysis are summarized as follows;
   - The products category in electornics, computers, and Home and kitcen accessories has higher potential for generating more revenue
   - The company should analyze and improve low revenue products or consider alternatives i.e. optimization, repositioning or discontinuation of the products.

### Recommendations

1. The company should tailor marketing strategies to the product category with high revenue productions
2. They should check/Re-evaluate what is not working by revising pricing, marketing or pricing positioning of the low revenue generated products
3. Monitor custmer feedback and market trends to drive sales growth and product success.
4. They need to allocate resources to maintain and grow sales.




   

   
   

   

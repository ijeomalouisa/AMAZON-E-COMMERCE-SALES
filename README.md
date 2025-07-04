## AMAZON E-COMMERCE SALES ANALYSIS
   
### THE PROJECT TOPIC: REVIEW ANALYSIS OF AMAZON PRODUCT
The review analysis of Amazon products on the project of Digital Skill-Up Africas given to me as a Junior Data Analyst. It is part of the prerequisit assignment that will inturn help me to up-skill my career and be rated as a data analyst. 

### PROJECT OVERVIEW:
Amazon is a company that provides E-commerce sales. They deals with different kinds of accessories ranging from electronics, computer/accessories, car and motor bikes accessories, helath and personal care medical equipments, musical instrument, office products, toys and games etc. This project will allow me to generate insight that can guide the company on product improvement,marketing strategies and customer engagement.

### DATA SOURCE:
**Amazon Sales Data:** The primary dataset used for this analysis is the "Amazon_Case_Study.xlsx" file. The dataset contains information from each sales which includes;
* Product details: name, category, price, discount and ratings
* Customer engagement: user reviews, titles, an contents.

### TOOLS USED: 
- Microsoft Excel (https://www.microsoft.com), other tools I used to explore are;
- Excel Power query (for cleaning of the data)
- Calculated columns (for creating new metrics of KPIs)
- Pivot Charts ( for visualizing of the summarized data)
- Pivot tables (to analyze the data from different angles to identify trends and patterns so as to make informed decision)

###  EXPLORATORY DATA ANALYSIS (EDA):
An Exploratory Data (EDA) was deployed using Excel tools and relevant techniques to the context of each analysis. I will explore the Amazon sales data to answer these key questions. 

##### Task Question 1:

The analysis will be based on the use of Pivot tables and calculated columns where necessary to answer the following;
  1. Find the average discount percentages by Product category
  2. Check how many products that are listed under each category
  3. Calculate the total number of review per category
  4. show product that has the highest average ratings
  5. Acertain the average actual prices Vs the discounted prices by category
  6. To List the products that have the highest number of reveiws
  7. Find how  many products that have a discount of 50% or more
  8. To show the distribution of product ratings i.e. how many products that are rated 3.0, 4.0 etc
  9. calculate the total potential revenue of actual price * rating count by category
  10. Find out the number of unique products per price range bucket e.g. <200, <200-500, >500
  11. To show how the rating relates to the level of discount
  12. Check how many products have fewer than 1,000 reviews
  13. Find out which categories have product with the highest discounts
  14. To identify the top 5 products in terms of rating and number of reviews combined
  
#### Task Question 2: Dashboard Creation
I will use the clean dataset with the pivot outputs and build an Excel dashboard to unleash beautiful creativity

### DATA CLEANING/PREPARATION (EXCEL)
In view of the preparation task concerning this product, I performed the followings: we have 2 options for the cleaning. We can go by writing functions/formular or use Excel power query, I choosed Power query instead. 
1. To "DATA" menu, "from get and transform data", click the table/range,
2. The data was loaded to the Excel power querry,
3. I viewed it to see the column quality, going through it, I observed that there was "NULL" and "ERROR" in the rating count. as far as am concerned the data is dirty.
4. I shortened the "category" aspect of the dataset to make it look good, if not, in the course of the analysis it may be too long.
5. Highlight and Right click on the category to choose split column by delimiter i.e. "left most delimiter", Ok, it splited it into two, in the computer and accessories writing together
7. Right click again to replace values i.e value to find "&" then replace with "space" (it will be divided into two)
8. HomeImprovement, MusicalIstrument and OfficeProduct are still together and they are the three arguments I added space
9. I Go to add column, "Conditional column", HomeImprovement, category 1, then HomeImprovement writing in space e.g. replace Home Improvement
10. add clause to repeat the remaining two i.e. MusicalInstrument and OfficeProduct, Else Category 1
11. In the product name, count the number of character, I counted and stoped at 25 character including the spaces,
12. split the column again BUT not by delimiter, Split by number of character "once as far left as posible"
13. add the 25 and check on "once as far left as possible
14. Right Click and remove the splited right column
15. change the data types
16. I removed columns that are not needed. i.e. the img link, user-name, review content and product link etc because they are not necessary.
17. Close and Load my query.

#### Steps taken for Data Cleaning: Here are some interesting codes used in the course of this Cleaning analysis
- conditional columns AND
- Custom Columns ... See below other steps; 





<img width="706" alt="AMAZON POWER QUERY" src="https://github.com/user-attachments/assets/4db12e29-4e8a-4bf2-960c-8a8c78600904" />


In all, eight (8) columns were deleted because it is not needed in the analysis and six (6) additional columns was created in addition to the important existing ones as it appears in the Amazon case study so as to tackled the two task questions simultenously.

NEW TABLES CREATED ARE SHOWN THUS:

* Price Range Bucket
* Discount Band
* High Discount
* Low Review
* Total Potential Revenue
* Combined Scores

Find attached the clean data set as it appears in the cleaned table.....


<img width="770" alt="AMAZON CLEANED TABLE" src="https://github.com/user-attachments/assets/22d947f5-583e-4501-a230-9ee2fa45baf8" />

#### Here are Some calculated Column funtions, if I was to clean the data with it: 
...xlsx

   To shorten the "Product Category":
   =IFERROR(LEFT(C2,FIND("&",C2)-1)C2)

   To calculate the Potential Revenue:
   =Sum(actual price * Rating count)

   For Price Range:
   = IF(actual price <200, "<200",IF(actual price<=500,"200-500",">500"))

   For More than 50% Discount:
   =IF(H2>=50%,">50%","<50%")

   **AMAZON POWER PIVOT TABLES:**


<img width="634" alt="AMAZON POWER PIVOT" src="https://github.com/user-attachments/assets/3cdced33-7698-45a9-8b10-5e7a348a0d32" />


   
### KEY METRICS ANALYSIS

These few metrics are analyzed and the graphs shown below in a power pivot;

*  Total number of Product
*  Total potential Revenue
*  Average Discount Percentages Per Product and
*  Total Reviews

 <img width="374" alt="KEY METRIC PRODUCTS" src="https://github.com/user-attachments/assets/f1851354-c205-4299-83a2-48d10e5f3e83" />



**PRODUCT RATINGS:**
The rating of the the above key metrics could be looked into taking cognizance of different diverse/effects such as; market influence, pricing, durability, government policies and seasonal influence. To rate the products, the company should consider using a simple framework.

#### INFERENCES:

This story will highlight the importance of product management and data driven decision making that can guide AMAZON COMPANY for product improvement, marketing strategies and customer engagement:

* Electronics, computer and accesories and home kitchen has a strong market demand as evidence in the number of products they sale, potential revenue generated, rating counts and the average discount percentages. This might be because of effective marketing and innovative solution, customers might be looking at the quality of the product (durability), this might be the cause of the increase in demand, delivery is also considered. Above all, the products remains the best seller with consistent sale growth.
*  Musical Instrument and office product has stable demand but there should be room for improvement, this I think may lead to expansion and niche market is strongly adviced.
*  Health & personal care, Home improvement has limited market interest which might be pricing issues. In this products, the needs arises once a while and not everyone pay attention to it except people that matters like hospital owned by government. Priviate hospital owned by individuals might refer patients if the equipment is not avaliable.
* Car & motorbike is everyones choice of product. A product that has high production cost but the economy i.e. government policies (tax, custom duties, wages and salary) has most influence on it. It is a low revenue product as it has limited market interest and delining sales, so the company needs to revise the pricing as well as marketing position.
* Toys & Games is a products that has limited market demand because it is mainly used by children and the sales has seasonal influence. The company needs to advertise the product in a physical market/Television mainly because most children don't order goods and services online as evidence in the company's sales.      


### FINDINGS AFTER INFERENCE:

There is a strong market demand of elecronics accessories, computer and accessories and Home kitchen accessories among the target audience. This could be because the pricing strategies is okay with the customers OR that the reviews drive sales. Also, the products has a competitive adavantage of unique values proposition/ features. This is evidenced in the High Revenue generated of Electronics accessories: #91,323,918,321.00, Computer Accessories: #11,628,224,483.38 and Home & Kitchen Accessories #10,457,243,329.00 respectively. Amazon Basics High-Speed Product(Product name) remains the product that has the highest number of reveiw as evidenced in sum of rating count of 853,946.00, BoAt Bassheads 100 in ear 772,426.00 and RedMi 9A Phone has 627,668.00. The company should tailor marketing strategies to the high revenue product categories with high revenue products. 

On This Other hand, There is a Low revenue generation in Toys & Games, Car & motor bike, home improvement, Health & personal care accessories. The inference might be because in the Categories, there is low demand from the audience or that the pricing strategy are not competitive. This is informed from the #2,380,050.00, #4,472,000.00, #6,163,434.00 and #6,959,700.00 revenue generated from the product categories. The company should monitor customers feedback and market trends to drive sales growth and success of this goods also revise the pricing, marketing positioning from there, what is not working might start working well. Serious advert is needed in category Toys & Games using animation that will appeal the children's eyes because these days most of them tend to go online and their mind signals at what they like most.


**SLICER/FILTERING**

**Real-time filtering across(Slicer) Product category, Price Range Buckect and High Discount**


<img width="335" alt="Slicers " src="https://github.com/user-attachments/assets/c0c5cd4e-3a9a-42ef-862a-a61a79d0bfe9" />

### TASK 2:   CREATION OF DASHBOARD 

This is a Dashboard created Using the Cleaned Dataset and Pivot Outputs:



<img width="388" alt="AMAZON DASHBOARD 2" src="https://github.com/user-attachments/assets/7d7b77e7-f3e2-497f-8369-90f8d1a439d7" />






The above Dashboard unleashed different creativity indicating a guide for data-driven decisions on marketing, resource allocation, pricing, most especially to derive sales growth and product features.


### CONCLUSION:
   The result of the analysis are summarized as follows;
   - The products category in electornics, computers, and Home and kitcen accessories has higher potential for generating more revenue
   - The company should analyze and improve low revenue products or consider alternatives i.e. optimization, repositioning or discontinuation of the products.

### RECOMMENDATIONS

1. The company should tailor marketing strategies to the product category with high revenue productions
2. They should check/Re-evaluate what is not working by revising pricing, marketing or pricing positioning of the low revenue generated products
3. Monitor custmer feedback and market trends to drive sales growth and product success.
4. They need to allocate resources to maintain and grow sales.




   

   
   

   

### AMAZON SALES ANALYSIS
This is where I will document the analysis made in the course of analyzing this Captstone project (Amazon_Case-Study)
   
### THE PROJECT TOPIC: REVIEW ANALYSIS OF AMAZON PRODUCT
Amazon product review analysis project of the Digital Skillup Africa (DSA) was given to me as a Junior Data Analyst. It is part of the prerequisit assignment that will inturn help me to up-skill my career and be rated as a data analyst. 

### PROJECT OVERVIEW:
Amazon is a company that provides E-commerce sales. They deals with different kinds of equipment/electronics and gadgets ranging from electronicsa and  accessorys, computer/accessories, car and motor bikes accessories, helath and personal care medical equipments, musical instrument, office products, toys and games etc. This data anlysis project allows to generate insight that can gide product improvement,marketing strategies and customer engagement of the company

### Data Source:
Amazon Sales Data: The primary dataset used for this analysis is the "Amazon_Case_Study.xlsX" file. lThe dataset contains information from each sales which includes;
* Product details: name, category, price, discount and ratings
* Customer engagement: user reviews, titles, an content

### Tool used: 
- Microsoft Excel (https://www.microsoft.com), other tools I used to explore are;
- Excel Power query (for cleaning of the data)
- Calculated columns (for creating new metrics of KPIs)
- Pivot Charts( for visualizing of the summarized data
- Pivot tables (to analyze the data from different angles to identify trends and patterns so as to make informed decision.

###  The Exploratory Data Analysis (EDA):
A Comprehensive Exploratory Data (EDA) were deployed using Excel tools and relevant techniques to the context of each analysis.
##### Task 1:
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
  #### Task 2: Dashboard Creation
  *    To use the cleare dataset and pivot outputs and build an Excel dashboard to unleash beautiful creativity

### Data Cleaning/Preparation (Excel):
The Amazon Casy study dataset undergo a cleaning section. we have 2 options for the cleaning. We can go by writing formular or use Excel power query, I choosed Power query instead. to "DATA" menu, from get and transform data, the table/range, the data was loaded to the Excel power querry, I viewed it to see the column quality, going through it, I observed that there was 1 error in rating count only. as far as am concerned the data is dirty. I shortened the "category" aspected of the dataset to make it look good if not, in course of the analysis it may be too long.

### Data Analysis:

- Highlit and Right click on the category to choose split column by delimiter i.e. "left most delimiter", Okay, it split it into two, in the computer and accessories writing together
- right click again to replace values i.e value to find & then replace with space (it will be divided into two
- HomeImprovement, MusicalIstrument and Officepractice are still together and they are the three arguments I added space
- Go to add column, "Conditional column", HomeImprovement, category 1, then HomeImprovement writing in space e.g. replace Home Improvement
- add clause to repeat the remaining two i.e. MusicalInstrument and OfficePractice
- Else Category 1
- in the product name, count the number of character, I counted and stoped at 25 character including the spaces,
- split the column again BUT not by delimiter, Split by number of character "once as far left as posible"
- add the 25 and check on "once as far left as possible
- Right Click and remove the splited right column
- change the data types
- I removed other columns that are not needed. the img link, user-name, review content and product link were removed because they are not necessary.

#### Writing calculated Column formulars: 
...xlsx

   To shortened the Product Category:
   =IFERROR(LEFT(C2,FIND("&",C2)-1)C2)

   To calculate the Potential Revenue:
   =Sum(actual price * Rating count)

   For Price Range:
   = IF(actual price <200, "<200",IF(actual price<=500,"200-500",">500"))

   For More than 50% Discount:
   =IF(H2>=50%,">50%","<50%")

   ### Results/Findings:

   
   

   

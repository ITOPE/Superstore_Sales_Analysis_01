# Sales Analysis

![Screenshot (388)](https://user-images.githubusercontent.com/84106015/218905224-47e1bce3-cdac-476b-b9e2-4940bcf9e0cd.png)

![Screenshot (389)](https://user-images.githubusercontent.com/84106015/218905259-ea4f7371-f948-4be4-92e7-3bd65f83b68a.png)

![Screenshot (390)](https://user-images.githubusercontent.com/84106015/218905277-343485e6-5fc9-47f1-8c86-e9ed8a33055b.png)


---


# Introduction

Superstore sales dataset, which spanned over the period of four years (2010 to 2013) was analyzed. 
The Revenue trends, profit trends and the consumer buying habit were analyzed in the sales cohort. From this analysis, actionable business insights were derived, which would be used to make data-driven business decisions by the company and in-turn lead to business growth and profitablity.  

The analysis provided answers to the following questions: .

- Which product category generated the highest revenue?
- Which product category generated the lowest revenue? How can this product performance be improved?
- Which country generated the highest sales? 
- Which country generated the lowest sales?
- What is our year over year growth rate? (Is the business growing?)
- What is the profitability status of the company?
- Which consumer segment generated the higbest revenue?
- Who are our top customers?
- What is the effect of price dicounting on sales performance?
---

# Observations and Insights

* The total revenue generated was $30, 069, 581.97. Year 2013 had the highest sales performance ($10,134,941.60), while year 2010 had the lowest sales permance     ($6,135,782.14). The revenue performance increased by 4.31% in year 2011, 15.60% in year 2012 and 36.99% in year 2013.
* The gross profit was $14, 818, 291.46. The profit margin was 50.06%. This implies the business is profitable (50.06% is a good profit margin according to the  industry standard). 
Bookcases had the highest profit margin (65.66%), while binders and binders accessories had the lowest profit margin (33%).
* The cumumulative year over year growth rate was 56.89%.
* There were 17 product categories. The telephone and communication category generated the highest sales $4,392,549.60 while the home and office category followed at a very close margin (4,322,5245.53).
* Our coustomers are classified under four diffent segments (Corporate, Consumer, Home Office and Small Business). The corporate segment generated the highest sales of $11, 226, 543.21, which constituted 37.34% of the total sales, followed by the home office segment, with total amount of $7, 127, 926.34(23.70%), then the small business $5, 917, 274.92(19.68%) and the consumer segment $5,797,837.50(19.28%).
Rubber band had the lowest performance, generating $30,901.47.
Joan Oakley Schaefer of the corporate segment was the top customer. He bought goods worth $207, 568.56.
* From the map chart we deduced that in North America, USA is the only contry where there was patronage and also the country that generated highest sales. in Asia, China led in sales generation.
* Table in the home and office consumer segment had the highest discount rate. From the discount chart, it can be deduced that discounts had no effect on products.
* The corporate consumer segment has consitently topped the chart from 2010 till 2013.
* From the revenue trend chart, we deduced that over time our sales peaks in November and mostly troughs in January.  Office machine in the cooperate segment is one of the products in high demand during the surge period.


# Conclusions and Recommendations
* The product awareness is very low in most countries. We should maximize our online presence.
 Also, our marketing teams in these countries should regularly organize brand awareness activities.
* Binders price can be increased a bit, we can also source for cheaper and efficient supplier of binders so as to reduce cost price. 
* For our least revenue generating product categories to have a good profit margin means they have good potentials, so we should do all necessary to boost their revenue generating power.
* The products in high demand during surge should be made readily available to avoid shortage.
* Discount didn't really have effect on revenue and profit, so it should be abolished.

---
# Developer Tool
Power Bi power query editor and  desktop was used to accomplish this project.

# Live Demo
https://raw.githack.com/ITOPE/Superstore_Sales_Analysis_01/main/Superstore1.pbix

# Procedure
Data was imported from excel workbook. In the power query editor in Power BI, we checked our dataset for null values, duplicates and outliers. We don’t have duplicates and any obvious outliers, but we have null values in the postal code column which we left since we won't be using the column.
We created our sales metrics using the following DAX formulas:

COGS = SUM(SuperstoreSalesTraining[Sales])-SUM(SuperstoreSalesTraining[Profit])

TY = SUM(SuperstoreSalesTraining[Sales])

LY = CALCULATE(All_Measures[TY],DATEADD(calender[Date].[Date], -1,YEAR))

LY1 = SUMX(VALUES(calender[Date].[Date]),All_Measures[LY])

YOY = DIVIDE(All_Measures[TY]-All_Measures[LY],All_Measures[LY],0)

YOY1 = SUMX(VALUES(calender[Date].[Year]),[YOY])

##### Note: Power Bi was displaying wrong total for "LY" and "YOY" in the measure table, so we created measures "LY1" and "YOY1" to rectify the issue.

I also created a calendar table using DAX expression "calendar = CALENDARAUTO()", and we created connections between the new calendar table and the superstoresalestraining table.
We then went ahead to create our visuals.



# Abbreviations

COGS= Cost of Goods Sold

TY= Total Year sales (same as Total Sales or Current Year)

LY= Last Year sales

YOY= Year over Year growth

# Background Template 

The background templates were created using Microsoft PowerPoint 2010.

# Prerequisites

Power Bi must be installed before this project can be carried out.
Power Bi must be updated for map visuals to work perfectly.

# Data Source
Kaggle

# Author

GitHub: ITOPE

LinkedIn: Itunu Fatokunbo

# Contribution 

Contributions, issues and requests are welcome!



# Superstore_Sales_Analysis_01

A Superstore sales dataset which spanned over the period of four years (2010 to 2013) was investigated. 
The sales overview, profit and trends in sales cohort was analyzed, so as to answer the following questions and in turn derive actionable business insights.

---
- Which product segments are generating high revenue? and how can we maximize them?
- Which product segment are generating low revenue? and how can we make improvement?
- From which country are we generating most revevue? 
- What is our year over year growth rate? (Is the business growing?)
- Are we maximizing our product prices to generate profit?
- Does discount affect our sales?
- Who are our top customers?
---

# Developer Tool

We used Power Bi desktop to accomplish this project.

# Live Demo

https://raw.githack.com/ITOPE/Superstore_Sales_Analysis_01/main/Superstore1.pbix

# Procedure

Data was imported from excel using the get data menu. 
In the power query editor in Power BI, we checked our dataset for null values, duplicates and outliers. We don’t have duplicates and any obvious outliers, 
but we have null values in the postal code column which we left since we won't be using the column.
We created our sales metrics using the following DAX formulas:

COGS = SUM(SuperstoreSalesTraining[Sales])-SUM(SuperstoreSalesTraining[Profit])

TY = SUM(SuperstoreSalesTraining[Sales])

LY = CALCULATE(All_Measures[TY],DATEADD(calender[Date].[Date], -1,YEAR))

LY1 = SUMX(VALUES(calender[Date].[Date]),All_Measures[LY])

YOY = DIVIDE(All_Measures[TY]-All_Measures[LY],All_Measures[LY],0)

YOY1 = SUMX(VALUES(calender[Date].[Year]),[YOY])

##### Note: Power Bi was displaying wrong total for "LY" and "YOY" in the measure table, so we created measures "LY1" and "YOY1" to rectify the issue.

We also created a calender table using DAX expression "calender = CALENDARAUTO()", and we created connections between the new calender table and
the superstoresalestraining table.

We then went ahead to create our visuals.

##Images
![Screenshot (13)](https://user-images.githubusercontent.com/84106015/162594055-1c9d694e-4ac4-47d0-ad0d-9d7c38f41512.png)
![Screenshot (11)](https://user-images.githubusercontent.com/84106015/162594058-2b139062-622b-40ea-9edd-8b8055e9a703.png)
![Screenshot (12)](https://user-images.githubusercontent.com/84106015/162594063-27a62663-86f6-4c63-bf08-faf43eaeade3.png)


## Conclusion and Recommendation

From our analysis, we were able to derive answers to our questions.

Out of 17 product categories that we have, each falling within four consumer segments, four product categories are doing excellently well, with the corporate segment leading in the 4 segments we have. while we have 6 least products. 

* We recommend that the marketing teams should be encouraged to embrace the act of cross-selling.  E.g a customer ordering for copiers and fax should be persuaded to order paper as well.

---

USA is leading in revenue generation as its generated 29% of the total revene in four years. Followed by china, generating 14%. Here we see majority of the countries are not doing well at all.

* Seems our product awareness is very low in most countries. We should maximize our online presence.
* Our marketing teams in these countries should regularly organize brand awareness activities. 

---

The year over year growth is encouraging, from 4% in 2011 to 16% in 2012 to 37% in 2013.

The profit margin for each product is good with 50% rate in four years. Binder’s profit margin is low when compared to its revenue generation and also low compared to other  products.

* Binders price can be increased a bit, we can also source for cheaper and efficient supplier of binders so as to readuce cost price. 
* For our least revenue generating product categories to have a good profit margin means they have good potentials, so we should do all necessary to boost their revenue generating power.

---

When we examine the trends over time, we notice our sales surges in November and mostly dip in January.  Office machine in the cooperate segment is one of the products in high demand during the surge period.

* The products in high demand during surge should be made readily available to avoid shortage.

---

Discount didn't really have effect on revenue and profit.

# Abbrevations

COGS= Cost of Goods Sold

TY= Total Year sales(same as Total Sales or Current Year)

LY= Last Year sale

YOY= Year Over Year growth

# Background Template 

Background templates were created using Powerpoint and saved in JPNG format.

# Prerequsites

Power Bi must be installed before this project can be carried out.
Power Bi must be updated for map visuals to work perfectly.

# Authors

GitHub: @ITOPE

# Contributing 

Contributions, issues and feature requests are welcome!



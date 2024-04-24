# Smartphone Sales Analysis
## Dataset Description
The dataset was obtained from Kaggle. You can download the data from this link: [Kaggle Dataset](https://www.kaggle.com/datasets/shubham2703/smartphone-retail-outlet-sales-data/data). This dataset captures the transactions of a fictional retail company over a fiscal year (2018–2019). It provides valuable insights into the sales of smartphone accessories. The dataset is organized into several columns, each representing different aspects of the transactions.
### Tools Used
- Power Query > Ceaning Data
- DAX on Power BI > Writing Formulas
- Power BI > Analyzing and Creating Visuals
## Objective
My objective of this Power BI project was to analyze smartphone retail sales data and uncover trends and patterns in smartphone accessory sales with the aim of answering the following questions:
1. What were the total sales, revenue, and profit for each fiscal year and how many smartphone accessories were sold in total?
2. Which payment type was predominantly used by customers?
3. Which payment type generated the highest revenue for the fiscal year?
4. Which fiscal year brought the highest revenue?
5. Which month and week experienced the highest sales?
6. What were the top 5 products that generated the highest sales for the fiscal year?
## Data Loading and Cleaning
The data loading and cleaning process for this project was done using Power Query. **Let’s take a view of the original dataset**

![Picture9](https://github.com/elizabethwanjiku703/Smartphone-Retail-Sales-Data-Analysis-Power-BI-/assets/66907478/a1675e5d-bddb-4635-979e-870fb4683113)

Power Query is a data transformation and data preparation tool that allows you to connect, combine, and refine data from various sources before loading it into Power BI for analysis.
To load the dataset into Power BI, follow these steps:
   - Click on “Get Data” in the Home tab.
   - Select the appropriate data source (e.g., Excel, CSV, etc.).
   - Choose the downloaded dataset file.
   - Open the file and select the desired sheet or table.
   - Apply any necessary data cleaning and transformation steps using Power Query.
   - 
![Picture1](https://github.com/elizabethwanjiku703/Smartphone-Retail-Sales-Data-Analysis-Power-BI-/assets/66907478/761ceffe-2f1e-476e-ac0a-a22ede822b95)

   - I loaded the cleaned dataset (above table) into Power BI for analysis
   - 
## Adding Columns
After cleaning and removing the unwanted column, I added the following Columns using the following DAX Formulas (See the Table below):
         ``` 
            1. Day of Week = WEEKDAY('SMARTPHONE RETAIL OUTLET SALE DATA'[Date],2)
            2. Day of Week Name = SWITCH('SMARTPHONE RETAIL OUTLET SALE DATA'[Day of Week],
             1, "Monday",
             2, "Tuesday",
             3, "Wednesday",
             4, "Thursday",
             5, "Friday",
             6, "Saturday",
             7, "Sunday"
         )
         ```
         
![Picture6](https://github.com/elizabethwanjiku703/Smartphone-Retail-Sales-Data-Analysis-Power-BI-/assets/66907478/f578aaa7-f45b-47f4-a577-d6e529fd398e)

## Data Exploration and Analysis

Since the data is ready, we can dive in creating visuals
   1. What were the total sales, revenue, and profit for each fiscal year and how many smartphone accessories were sold in total?
```
Sales = SUM('SMARTPHONE RETAIL OUTLET SALE DATA'[Amount])

Revenue = SUMX('SMARTPHONE RETAIL OUTLET SALE DATA','SMARTPHONE RETAIL OUTLET 
             SALE DATA'[Quantity]*'SMARTPHONE RETAIL OUTLET SALE DATA'[Price])

Profit = SUM('SMARTPHONE RETAIL OUTLET SALE DATA'[Price])

Products Sold= COUNT('SMARTPHONE RETAIL OUTLET SALE DATA'[Product Number])
```
![1](https://github.com/elizabethwanjiku703/Smartphone-Retail-Sales-Data-Analysis-Power-BI-/assets/66907478/0f55285f-ab28-4226-ba23-4de103d58eef)

### Insights
The total sales for the period were $123.64 million. The profit generated during this time was $117.47 million, and the revenue reached $119.85 million. The total number of products sold was 6,421. These figures provide a snapshot of the financial performance, indicating strong sales and profitability for the given fiscal year period.

   2. Which payment type was predominantly used by customers?
   3. 
![2](https://github.com/elizabethwanjiku703/Smartphone-Retail-Sales-Data-Analysis-Power-BI-/assets/66907478/0b7f86de-c340-4364-954e-494a028facd4)

In the provided image, a clustered bar chart was utilized to depict the total transactions. The design approach adopted for this visualization followed the comprehensive and instructive guideline presented by @Bas on his YouTube channel, [“How to Power BI”](https://www.youtube.com/@HowtoPowerBI). I highly recommend checking out his channel as it offers valuable insights on design principles and other aspects pertaining to Power BI.

### Insights
Mobile payments were the most preferred method with 1,832 transactions, indicating the growing popularity of convenient digital payment options. Debit cards followed closely with 1,787, Credit cards were also widely utilized, with a count of 1,630 transactions, and Cash transactions totaled 1,172, suggesting that while digital payments are on the rise, physical currency still holds significance for certain customers.

   5. Which payment type generated the highest sales for the fiscal year?

![3](https://github.com/elizabethwanjiku703/Smartphone-Retail-Sales-Data-Analysis-Power-BI-/assets/66907478/a06d5b07-217b-4e8c-918a-10aead44d68a)

### Insights
Debit payment emerged as the front-runner in terms of generating sales, amounting to an impressive $38.53 million. This indicates that customers showed a strong preference for utilizing their debit cards when making purchases in the retail outlet.

   7. Which fiscal year brought the highest revenue?

![4](https://github.com/elizabethwanjiku703/Smartphone-Retail-Sales-Data-Analysis-Power-BI-/assets/66907478/96d996f6-7050-4101-81cf-7f27d41f2e48)

### Insights
The fiscal year 2021–2022 emerged as the most lucrative period, generating a substantial revenue of $44.18 million, indicating high demand for smartphone accessories. However, the fiscal year 2022–2023 experienced a decline in revenue of $1.77M, possibly due to changing market conditions, shifts in consumer preferences, or increased competition.

   9. Which month and week experienced the highest sales?

![5](https://github.com/elizabethwanjiku703/Smartphone-Retail-Sales-Data-Analysis-Power-BI-/assets/66907478/468e1cd0-be61-447a-a993-bc022c6ac3da)

### Insights
a. July emerged as the highest-selling month across all fiscal years, with total sales reaching an impressive $18 million This observation suggests that customers tend to make more purchases during the period between April and September, which typically has fewer holidays or celebrations. The absence of major holidays during this time may contribute to increased customer buying behavior.
b. When analyzing the weekly sales patterns, it was found that Sunday experienced the highest sales, while Monday and Tuesday recorded the lowest sales. This trend could be attributed to various factors, such as weekend shopping habits or promotional activities that are often held on Sundays. Understanding these weekly sales patterns can help businesses strategically plan their marketing initiatives and allocate resources accordingly.

   11. What were the top 5 products that generated the highest sales for the fiscal year?

![6](https://github.com/elizabethwanjiku703/Smartphone-Retail-Sales-Data-Analysis-Power-BI-/assets/66907478/c707472d-32af-4d9a-a7ba-6c528e9c2863)

### Insights
- The sales figures indicate that midrange phones generated the highest revenue, followed closely by flagship phones. This suggests that there is a significant demand for both affordable and high-end devices.
- Budget phones also contributed a substantial amount to the overall sales, indicating that there is a market for more affordable options with decent performance.
- The sales of premium midrange and luxury phones, although lower in comparison, still demonstrate a demand for devices with premium features and designs.
## Creating a Dashboard
Introducing our comprehensive sales dashboard, where we bring together all the insightful analysis of our fiscal year’s performance. This interactive and visually appealing dashboard provides a holistic view of sales and their corresponding revenue figures.
![Dashboard](https://github.com/elizabethwanjiku703/Smartphone-Retail-Sales-Data-Analysis-Power-BI-/assets/66907478/419f0e36-2bb0-4b6c-8d98-7b19c3002271)
## Recommendation
- To begin, it is crucial for the company to invest in enhancing its marketing efforts during quarters 2 and 3. These periods represent prime opportunities to entice more customers to make purchases.
- Furthermore, it appears that the months of July to September witness a surge in consumer spending. Therefore, it is advisable to allocate more resources to marketing during this period.
- They can offer exclusive promotions and incentives in coming years, since fiscal year 2020–2023 had the lowest revenue.






















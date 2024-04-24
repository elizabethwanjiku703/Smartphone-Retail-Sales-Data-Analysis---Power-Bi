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
![Picture1](https://github.com/elizabethwanjiku703/Smartphone-Retail-Sales-Data-Analysis-Power-BI-/assets/66907478/761ceffe-2f1e-476e-ac0a-a22ede822b95)
   - I loaded the cleaned dataset (above table) into Power BI for analysis
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













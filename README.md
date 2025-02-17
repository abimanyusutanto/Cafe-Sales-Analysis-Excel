# **Cafe Sales Analysis**

## **Project Overview**

This project focuses on cleaning, analyzing, and extracting valuable insights from café sales data to better understand customer behavior, product demand, and sales trends. The dataset contains transactional data, including product sales, payment methods, locations, and dates, which are processed and analyzed using Microsoft Excel.

The primary goal of this project is to transform raw sales data into a structured and insightful dataset that helps in making data-driven business decisions. This involves identifying missing values, correcting inconsistencies, standardizing formats, and creating interactive visualizations that allow stakeholders to easily interpret the data. Information about the dataset used can be seen [here](https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training)

## **Objectives**

- Clean and standardize the dataset by handling missing values, correcting inconsistencies, and formatting dates.
- Analyze sales performance by identifying top-selling products, preferred payment methods, and sales trends.
- Develop an interactive dashboard to visualize key insights and support data-driven decisions.

## **Data Cleaning Process**

1. Eliminated duplicate records to maintain data integrity and avoid skewed analysis.
2. Handle Missing Values (Quantity, Price Per Unit, Total Spent) by removing rows where at least two of these three columns were missing since the total cost could not be calculated.
3. Fill Missing Values in Sales Data:
    - Filled missing Quantity using $\frac{\text{Total Spent}}{\text{Price Per Unit}}$
    - Filled missing Price Per Unit using $\frac{\text{Total Spent}}{\text{Quantity}}$
    - Filled missing Total Spent using $\text{Quantity} \times \text{Price Per Unit}$
4. Matched missing Item values based on existing Price Per Unit data.
5. Used RANDBETWEEN in Payment Method clumn to assign a random value (Cash, Credit Card, or Digital Wallet) in a 1:1:1 ratio due to no significant distribution difference.
6. Used RANDBETWEEN in Location column to assign a random value (In-store or Takeaway) in a 1:1 ratio.
7. Dropped rows where Transaction Date was missing since it was a critical timestamp.
8. Extracted the month from Transaction Date to support time-based analysis in the dashboard.

## **Data Visualization**

![image](https://github.com/user-attachments/assets/c45a4054-3046-4741-86d6-7aaf7387e0c1)

The Cafe Sales Dashboard provides a comprehensive analysis of the café’s sales performance, helping stakeholders understand key trends and insights. By visualizing sales data, this dashboard allows for better decision-making regarding product demand, customer behavior, and revenue growth.

By analyzing this data, café owners and managers can optimize inventory, adjust marketing strategies, and improve customer experience to boost overall sales and profitability.

Now, let’s break down each chart and KPI in detail.

1. **Sales by Item**

   ![image](https://github.com/user-attachments/assets/7c72378b-6b12-4abc-92c3-ac97998e9a28)

   Explanation :
   - This chart displays the total sales by item type sold in the café.
   - Each item, such as Sandwich, Juice, Coffee, Salad, Cake, Cookie, Tea, and Smoothie, is shown based on the total quantity sold.
   - The best-selling item appears to be Sandwich, while Smoothie has the lowest sales.
   
   Insights :
   - The top-selling items can help determine inventory and promotional strategies.
   - Low-performing items can be analyzed to decide whether to discontinue them or offer discounts.
   
2. **Total Revenue**

   ![image](https://github.com/user-attachments/assets/e46027ef-633b-4b51-bebd-c9d629214acf)

   Explanation :
   - Displays the total revenue generated from all transactions.
   - Value: $84,551 represents the total sales income for the café.
   
   Insights :
   - This metric serves as a primary indicator of the café’s overall performance.
   - Comparing it with previous periods can help determine growth or decline in revenue.
   
3. **Total Transaction**

   ![image](https://github.com/user-attachments/assets/5e4b3d8b-52ca-4a42-8f62-98d3645b0f2e)

   Explanation :
   - Value: 9,475 indicates the total number of transactions recorded in the café during the analyzed period.
   
   Insights :
   - This number provides insight into how frequently customers purchase from the café.
   - Comparing it with total revenue helps determine whether customers are making small or large purchases per transaction.
   
4. **Average Spending**

   ![image](https://github.com/user-attachments/assets/7a1f50ab-e2b2-4e21-81fe-6c7970b64c14)

   Explanation :
   - Value: $8.92 represents the average amount spent per transaction.
   - It is calculated using the formula:

      $\
      \text{Average Spending} = \frac{\text{Total Revenue}}{\text{Total Transactions}}
      \$
   
   Insights :
   - If this value is lower than expected, strategies such as upselling or bundle offers may be necessary.
   - If it increases, it suggests that customers are buying higher-priced items or larger quantities per order.
   
5. **Sales by Payment Method**

   ![image](https://github.com/user-attachments/assets/25c203a0-2cc6-409d-b79d-1fb59797afd1)

   Explanation :
   - This chart shows the distribution of transactions by payment method.
   - The three main payment methods are:
         - Cash
         - Credit Card
         - Digital Wallet (which has the highest transaction count).
   
   Insights :
   - Digital Wallet is the most popular payment method, suggesting that customers prefer cashless transactions.
   - To encourage more transactions, the café could offer discounts for Digital Wallet payments or introduce cashback promotions.
   
6. **Revenue Trend Over Time**

   ![image](https://github.com/user-attachments/assets/f9b473dd-2821-4a8e-a293-c7e4381501e6)

   Explanation :
   - This chart displays monthly revenue trends throughout the year.
   - Certain months show an increase or decrease in revenue.
   - Example:
       - March and October have the highest revenue peaks.
       - February and November show slight declines in revenue.
   
   Insights :
   - High-revenue months should be analyzed to identify effective promotions or external factors influencing sales.
   - Low-revenue months should be targeted with stronger marketing strategies to boost sales.

## **Conclusion**

The Cafe Sales Analysis provides valuable insights into the café’s sales performance, customer preferences, and revenue trends. By leveraging data cleaning techniques and visualization, we transformed raw transactional data into meaningful business insights.

Key takeaways from the analysis:

- Sandwich is the best-selling item, while Smoothie has the lowest sales. This information can help with inventory management and promotional strategies.
- Total revenue of $84,551 and 9,475 transactions indicate the café’s overall financial performance and customer engagement.
- Average spending per transaction is $8.92, which helps assess customer purchasing behavior. Strategies such as upselling or discounts can be implemented to increase this value.
- Digital Wallet is the most preferred payment method, suggesting a growing trend toward cashless transactions. The café can encourage more digital payments through incentives.
- Revenue fluctuates across months, with peaks in March and October. Identifying the factors behind these trends can help plan marketing campaigns during slow months.

By using these insights, café owners and managers can optimize their operations, improve customer experience, and develop data-driven strategies to increase sales and profitability. This project demonstrates the power of data analytics in making informed business decisions.

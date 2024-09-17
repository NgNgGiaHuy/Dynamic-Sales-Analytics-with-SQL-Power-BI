# [PROJECT] Dynamic Sales Analytics with SQL & Power BI

## Introduction

A Sales Director wants an online dashboard to clearly understand how many products have been sold, who the customers are, and how sales have progressed over time. Additionally, he wants to focus on two categories: products and customers, as each employee has to work with different products and customers. This manager has sent a budget file to compare values with performance. Therefore, I have proposed the following user story:
  
As a Sales Director: He wants an overview dashboard of online sales to get a comprehensive view of sales performance, allowing him to track which customers and products are the best sellers. Additionally, he wants to monitor sales performance against the set budget. Therefore, I will create a dashboard that can update sales data daily and compare sales performance against the budget.
  
As a Sales Employee: They want a detailed view of online sales by customer and product to track which customers buy the most and identify potential customers. Additionally, they want to monitor the best-selling products. Therefore, I propose a dashboard that allows filtering data by customer and product, and also filtering customers by the products they have purchased.

Below is a demo of the final product that has been and is being developed for this project:

<table>
  <tr>
    <td style="text-align: center;">
      <img src="https://github.com/user-attachments/assets/7c61aeb8-facb-4ee1-b46e-ede7ed92082a" alt="Picture 4" style="width: 100%; max-width: 300px; height: auto;">
    </td>
    <td style="text-align: center;">
      <img src="https://github.com/user-attachments/assets/7d48d444-43e6-4dd6-8550-f5f036fd9f19" alt="Picture 3" style="width: 100%; max-width: 300px; height: auto;">
    </td>
  </tr>
  <tr>
    <td style="text-align: center;">
      <img src="https://github.com/user-attachments/assets/70ae98cf-1677-4734-9b4e-a43e8e27ea36" alt="Picture 2" style="width: 100%; max-width: 300px; height: auto;">
    </td>
    <td style="text-align: center;">
      <img src="https://github.com/user-attachments/assets/e5effc84-5df0-4082-b500-3cf9d4cd2121" alt="Picture 1" style="width: 100%; max-width: 300px; height: auto;">
    </td>
  </tr>
</table>
  
## The ways to do

The data I am using is Microsoft’s sample data: AdventureWorksDW2019 and the budget data file in Excel format that I have pushed.

### Select necessary data & Clean the data
- To meet the outlined requirements, I need to select the necessary data from the vast amount of data included in the sample dataset.
- After selecting the required dataa tables, I proceed to clean the dataa using SQL Sever. I have pusshed the queries to my GitHub and below are the results after executing them:

<p align="center">
  <img src="https://github.com/user-attachments/assets/31cee780-6eb2-49c0-a3b3-5886b8ad9ae9" alt="Picture 5" style="max-width: 100%; height: auto;">
  <br>
  <i>Dim_Calendar</i>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/f10ad301-53c1-4d5f-a830-956401bb9eef" alt="Picture 6" style="max-width: 100%; height: auto;">
  <br>
  <i>Dim_Customers</i>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/f60ff2c0-41bc-4437-9a2d-d97fb55c55b2" alt="Picture 7" style="max-width: 100%; height: auto;">
  <br>
  <i>Dim_Products</i>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/87852e90-7e4d-4919-914b-137374185344" alt="Picture 8" style="max-width: 100%; height: auto;">
  <br>
  <i>Fact_InternetSales</i>
</p>

After obtaining the query results, we save the data in `.csv` format for using in the next step of visualization. Below are some results after saving the data for visualization preparation.
<p align="center">
  <img src="https://github.com/user-attachments/assets/7c8bd812-5dcc-4ad0-9460-b24301ad2128" alt="Picture 9" style="max-width: 100%; height: auto;">
  <br>
  <i>Dim_Calendar.csv</i>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/312ca487-e8e3-4c0c-a65e-d5a74ddad481" alt="Picture 10" style="max-width: 100%; height: auto;">
  <br>
  <i>Dim_Customers.csv</i>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/d6cd9360-a95c-44b8-a093-e83e50b3b105" alt="Picture 11" style="max-width: 100%; height: auto;">
  <br>
  <i>Dim_Products.csv</i>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/dda81eae-a59c-4d18-bed5-936e4963535f" alt="Picture 12" style="max-width: 100%; height: auto;">
  <br>
  <i>Fact_InternetSales.csv</i>
</p>

### Import data, Build Data Model & Visualize data

#### Import data

After saving the query results as `.csv`, we proceed to import the data into Power BI. Since the data has already been cleaned during the querying process, no further adjustments are needed.

#### Build Data Model

We need to link the Dim tables with the Fact table using primary and foreign keys for each table.

<p align="center">
  <img src="https://github.com/user-attachments/assets/70ae98cf-1677-4734-9b4e-a43e8e27ea36" alt="Picture 2" style="max-width: 100%; height: auto;">
  <br>
  <i>Data Model</i>
</p>

#### Visualize data

After building the model, we create a place to store Measures and use DAX functions to calculate the Measures that meet the requirements of the problem.

Choosing the right chart for visualization can be quite challenging, as everyone has different visualization preferences. However, make sure to meet the requirements of the problem. You can refer to the charts I use, and if there are any mistakes, please provide feedback so I can improve myself! :sweat_smile:

<p align="center">
  <img src="https://github.com/user-attachments/assets/e5effc84-5df0-4082-b500-3cf9d4cd2121" alt="Picture 1" style="max-width: 100%; height: auto;">
  <br>
  <i>Demo Dashboard</i>
</p>

## Conclusion

The final product you receive is a dashboard that can track sales, customers, and products as outlined in the requirements.

As I am a student with limited experience in this field, I sincerely hope everyone will welcome and provide feedback to help me improve every day. Wishing everyone good health and lots of luck! :relaxed:

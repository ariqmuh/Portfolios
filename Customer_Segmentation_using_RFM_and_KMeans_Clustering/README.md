# Customer Segmentation using RFM and K-Means Clustering
In this project, we put ourselves as a  part of the Data Scientist Team of Olist, e-commerce in Brazil. 
We are assigned to help the marketing team to create segmentation of Olist customers based on their behavior.

## 🔸 Dataset Source: 
Kaggle [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/olistbr/brazilian-ecommerce)

## 🔸 Business Problem: 
Business Problem :
- How to segment the customers at Olist marketplace so we can divide customers based on their shopping behaviour?
- What kind of treatment for each cluster to increase retention rate customer?

## 🔸 Data Schema:
<p align="center">
  <img src="https://user-images.githubusercontent.com/82768391/139534021-9f3203f9-166b-4b76-8451-cc74b9c460d4.png" />
</p>

## 🔸 Attribute Information:
<table>
  <tr>
    <th>Attribute</th>
    <th>Data Type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>order_id</td>
    <td>object</td>
    <td>order unique identifier</td>
  </tr>
  <tr>
    <td>order_purchase_stamp</td>
    <td>datetime64[s]</td>
    <td>shows the purchase timestamp.</td>
  </tr>
  <tr>
    <td>order_item_id</td>
    <td>float64</td>
    <td>sequential number identifying number of items included in the same order.</td>
  </tr>
  <tr>
    <td>product unique identifier</td>
    <td>object</td>
    <td>product unique identifier</td>
  </tr>
  <tr>
    <td>payment_type</td>
    <td>object</td>
    <td>method of payment chosen by the customer.</td>
  </tr>
  <tr>
    <td>payment_value</td>
    <td>float64</td>
    <td>transaction value.</td>
  </tr>
  <tr>
    <td>review_score</td>
    <td>float64</td>
    <td>note ranging from 1 to 5 given by the customer on a satisfaction survey</td>
  </tr>
  <tr>
    <td>customer_unique_id</td>
    <td>object</td>
    <td>unique identifier of a customer</td>
  </tr>
  <tr>
    <td>product_category_name_english</td>
    <td>object</td>
    <td>category name in English</td>
  </tr>
  <tr>
    <td>month_order</td>
    <td>object</td>
    <td>month of order</td>
  </tr>
  <tr>
    <td>weekday_order</td>
    <td>object</td>
    <td>weekday of order</td>
  </tr>
  <tr>
    <td>month_year_order</td>
    <td>period[M]</td>
    <td>month and year of order</td>
  </tr>

</table>

## 🔸 Workflow:
1. Data Merging
2. Data Cleaning and Data Pre-processing
3. Exploratory Data Analysis (EDA)
4. Modeling (K-Means Clustering using RFM)
5. Conclusion
6. Business Recommendation

## 🔸 Modeling:
In the modelling section, the features we use are Recency, Frequency, and Monetary from customers. These three things can describe the transaction behaviour of a customer. The meaning of RFM itself is:
- Recency: The last time the customer made a purchase
- Frequency: Number of transactions
- Monetary: The spending power of a customer
 
By using the RFM feature, we use the K-Means Clustering algorithm to perform customer segmentation.

<p align="center">
  <img src="https://user-images.githubusercontent.com/82768391/139535367-5376055a-6517-4971-94c4-43b35b824edc.png" width="500" />
</p>
Based on the Elbow Method, we choose 4 clusters.

## 🔸 Result:
<p float="left">
  <img src="https://user-images.githubusercontent.com/82768391/139534544-c8edd881-1270-4106-a829-a4e67c2cfba8.png" width="500" />
  <img src="https://user-images.githubusercontent.com/82768391/139534768-765751c3-72f1-472c-9e30-b35eeac23228.png" width="500" /> 
</p>

|                 | recency | frequency | monetary |
|-----------------| ------- | --------- | -------- |
| Best Customers  |  207.85 |   11.40   | 27733.93 |
| Loyal Customers | 236.80  | 3.97      | 1141.96  |
| New Customers   | 132.46  | 1.11      | 170.77   |
| Lost Customers  | 392.97  | 1.11      | 170.48   |


## 🔸 Business Recommendation:
| RFM Segment             | Description                                                                                               | Strategy                                                             |
|-------------------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Best Customers          | Made transactions recently, made more than 1 transaction, and had the highest total transactions.         |  Loyalty program/reward points, new product recommendations, and exclusive product offers. (Cross / Up-Selling Strategy)|
| Loyal Customers         | made transactions recently, made more than 1 transaction, and had the high total transactions.            |  loyalty program/reward points and new product recommendations(Cross / Up-Selling Strategy)    |    
| New Customers           | Made transactions recently, made only 1 transaction, and had the low total transactions.                  | Welcome e-mail to build the relationship, offer loyalty program/reward points, and discount vouchers (Cross/Up-Selling Strategy) |
| Lost Customers          | Not made a transaction for a long time, made only 1 transaction, and had the lowest total transactions.   |  Regular limited offers, discount vouchers, campaign via e-mail and asking for feedback. (Retention & Reactivate Strategies)

## 🔸 Reference:
* <sup>[1]</sup> https://towardsdatascience.com/customer-segmentation-in-online-retail-1fc707a6f9e6
* <sup>[2]</sup> https://www.barilliance.com/rfm-analysis/
* <sup>[3]</sup> https://www.kaggle.com/farrasalyafi/eda-customer-segmentatioin
* <sup>[4]</sup> https://medium.com/analytics-vidhya/customer-segmentation-with-rfm-analysis-kmeans-clustering-32c387d04dfe

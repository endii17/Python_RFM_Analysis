# [PYTHON] RFM Analysis
## I. Introduction
### 1. About RFM Analysis
### Why RFM?
- RFM is a marketing analysis technique that stands for Recency, Frequency, and Monetary Value.
  - **Recency**: measures how recently a customer has made a purchase.
  - **Frequency**: measures how often a customer has made purchases.
  - **Monetary Value**: measures the total amount of money a customer has spent on purchases.
- RFM is used to identify and categorize customers based on their purchasing behavior and how recently and frequently they have made purchases, as well as the monetary value of those purchases.
### How?
- In RFM analysis, customers are scored based on three factors (Recency - how recently, Frequency - how often, Monetary - how much), then labeled based on the combination of RFM scores
### Reference
- [RFM Analysis For Successful Customer Segmentation](https://www.putler.com/rfm-analysis)
  
### 2. Business question
- SuperStore is a global retail company. The Marketing Department wants to run marketing campaigns during the Christmas and New Year holidays to thank customers for their past support of the company. In addition, potential customers can be upgraded to become loyal customers.
- The Marketing Director also proposed a plan to use the RFM model in Python to segment customers, and then launch marketing campaigns to thank customers for supporting the company over the past time. As well as exploit potential customers to become loyal customers.
- Suggestions to the Marketing and Sales team with the company's retail model, which of the three indicators R, F, and M should be most interested in?

### 3. Data description
| Description |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InvoiceNo: Invoice number. Nominal, a 6-digit integral number uniquely   assigned to each transaction. If this code starts with letter 'C', it   indicates a cancellation. |
| StockCode:   Product (item) code. Nominal, a 5-digit integral number uniquely assigned to   each distinct product.                                                         |
| Description:   Product (item) name. Nominal.                                                                                                                               |
| Quantity:   The quantities of each product (item) per transaction. Numeric.                                                                                                |
| InvoiceDate:   Invoice Date and time. Numeric, the day and time when each transaction was   generated.                                                                     |
| UnitPrice:   Unit price. Numeric, Product price per unit in sterling.                                                                                                      |
| CustomerID:   Customer number. Nominal, a 5-digit integral number uniquely assigned to each   customer.                                                                    |
| Country:   Country name. Nominal, the name of the country where each customer resides.                                                                                     |

## II. Data Wrangling
### 1. Explore Data

![image](https://github.com/user-attachments/assets/0f930cc9-7928-4d36-bda0-41ed1c782447)

### 2. Clean, Handle, Correct data types and Filter data 

![image](https://github.com/user-attachments/assets/abe9206d-bb05-4a33-a64d-94c0148e4e6b)

## III. Creating RFM score
### 1. Calculate RFM

![image](https://github.com/user-attachments/assets/b6695d4c-0b53-4cad-94f2-d3842abc9287)

### 2. Join with Segments

![image](https://github.com/user-attachments/assets/d4b906e1-bbd6-4d4e-872a-b823a43a84e6)
![image](https://github.com/user-attachments/assets/f522c482-468f-4d80-8d49-ec30d972b94a)

## IV. Visualization

![image](https://github.com/user-attachments/assets/bdcb6821-db1c-4afa-bc1e-dc23cd39067c)
![image](https://github.com/user-attachments/assets/97003c7b-9365-4895-b447-43f55381664f)
![image](https://github.com/user-attachments/assets/0dc2aae3-46a1-4b4c-aec6-b762773f1f88)
![image](https://github.com/user-attachments/assets/2a6d97a4-5194-4b07-900b-c2d0558a336e)
![image](https://github.com/user-attachments/assets/36142495-7836-4146-a6f5-d134f1e32591)
![image](https://github.com/user-attachments/assets/3a28d107-e520-47dd-abd8-be7b7618ae14)

## IV. Insights and Recommendations

- Firstly, among above 4000 customers, the Champion customer segment accounts for the largest number (19.04%). The 2nd and 3rd are the Hibernating and Lost customers (16.32% and 11.32% respectively). In contrast with the Cannot Lose Them segment, just about 2.12%.

- Secondly, based on the Total Sales view, the highest total sales belongs to the Champion segment, which accounts for above half of all segment (62.52%). The same with customer count, the Cannot Lose Them segment still has the lowest total sales with just 2.12%


| Segment               | Characteristics                                                                                 | Recommendation                                                                                    |
|-----------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Champions             | Bought recently, buy often and spend the most!                                                  | Reward them. Can be early adopters for new products. Will promote your brand.                     |
| Loyal                 | Spend good money with us often. Responsive to promotions.                                       | Upsell higher value products. Ask for reviews. Engage them.                                       |
| Potential Loyalist    | Recent customers, but spent a good amount and bought more than once.                            | Offer membership / loyalty program, recommend other products.                                     |
| New customers         | Bought most recently, but not often.                                                            | Provide on-boarding support, give them early success, start building relationship.                |
| Promising             | Recent shoppers, but haven’t spent much.                                                        | Create brand awareness, offer free trials                                                         |
| Need attention        | Above average recency, frequency and monetary values. May not have bought very recently though. | Make limited time offers, Recommend based on past purchases. Reactivate them.                     |
| About to sleep        | Below average recency, frequency and monetary values. Will lose them if not reactivated.        | Share valuable resources, recommend popular products / renewals at discount, reconnect with them. |
| At risk               | Spent big money and purchased often. But long time ago. Need to bring them back!                | Send personalized emails to reconnect, offer renewals, provide helpful resources.                 |
| Cannot lose them      | Made biggest purchases, and often. But haven’t returned for a long time.                        | Win them back via renewals or newer products, don’t lose them to competition, talk to them.       |
| Hibernating customers | Last purchase was long back, low spenders and low number of orders.                             | Offer other relevant products and special discounts. Recreate brand value.                        |
| Lost customers        | Lowest recency, frequency and monetary scores.                                                  | Revive interest with reach out campaign, ignore otherwise.                                        |




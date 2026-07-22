# Customer Cluster Analysis Report
## Date: December 2023
## Total Customer Base: 1000

# Executive Summary
The customer base consists of 1000 customers, segmented into four distinct clusters based on their demographic and behavioral data. The segment distribution is as follows: Cluster 0 (9.2%), Cluster 1 (25.9%), Cluster 2 (26.0%), and Cluster 3 (38.9%). Key findings include:
* Cluster 1 has the highest frequency of purchases and average spend, indicating a loyal customer base.
* Cluster 2 has the highest average income and spend, presenting an opportunity for premium product offerings.
* Cluster 3 has the largest customer count, but lower average spend and frequency, suggesting a need for targeted marketing campaigns to increase engagement.

# Segment Analysis
### Cluster 0: "Casual Shoppers"
* Customer Count: 92 (9.2%)
* Avg Age: 39.5 years
* Avg Income: $67,945.60
* Avg Recency (Days since last purchase): 107.3 days
* Avg Frequency (Purchases in 6mo): 2.4 purchases
* Avg Spend (Monetary value in 6mo): $202.73
* Avg Session Duration: 468.0 seconds
* Avg Pages Viewed per Session: 5.2
Casual Shoppers are less frequent buyers with lower average spend. They require targeted marketing efforts to increase purchase frequency and engagement.

### Cluster 1: "Young Enthusiasts"
* Customer Count: 259 (25.9%)
* Avg Age: 23.7 years
* Avg Income: $46,758.16
* Avg Recency (Days since last purchase): 20.1 days
* Avg Frequency (Purchases in 6mo): 6.9 purchases
* Avg Spend (Monetary value in 6mo): $344.49
* Avg Session Duration: 685.2 seconds
* Avg Pages Viewed per Session: 8.0
Young Enthusiasts are frequent buyers with high engagement. They are ideal targets for loyalty programs and social media marketing campaigns.

### Cluster 2: "Affluent Buyers"
* Customer Count: 260 (26.0%)
* Avg Age: 42.7 years
* Avg Income: $70,264.52
* Avg Recency (Days since last purchase): 17.4 days
* Avg Frequency (Purchases in 6mo): 7.2 purchases
* Avg Spend (Monetary value in 6mo): $627.55
* Avg Session Duration: 457.3 seconds
* Avg Pages Viewed per Session: 4.9
Affluent Buyers have high average income and spend. They are likely to respond to premium product offerings and personalized marketing campaigns.

### Cluster 3: "Mainstream Customers"
* Customer Count: 389 (38.9%)
* Avg Age: 43.5 years
* Avg Income: $70,335.72
* Avg Recency (Days since last purchase): 23.3 days
* Avg Frequency (Purchases in 6mo): 3.9 purchases
* Avg Spend (Monetary value in 6mo): $312.52
* Avg Session Duration: 467.1 seconds
* Avg Pages Viewed per Session: 5.0
Mainstream Customers are the largest segment, but have lower average spend and frequency. They require targeted marketing efforts to increase engagement and loyalty.

# Actionable Business Recommendations
### Cluster 0: "Casual Shoppers"
1. **Re-engagement Campaigns**: Send targeted email campaigns to inactive customers to encourage repeat purchases.
2. **Personalized Offers**: Provide personalized product recommendations based on purchase history to increase average spend.
3. **Loyalty Program**: Introduce a loyalty program to reward frequent buyers and increase customer retention.

### Cluster 1: "Young Enthusiasts"
1. **Social Media Campaigns**: Launch social media campaigns to engage with Young Enthusiasts and increase brand awareness.
2. **Influencer Partnerships**: Partner with social media influencers to promote products and increase reach.
3. **Exclusive Offers**: Offer exclusive discounts and promotions to Young Enthusiasts to increase loyalty and retention.

### Cluster 2: "Affluent Buyers"
1. **Premium Product Offerings**: Introduce premium products and services to cater to Affluent Buyers' high average income and spend.
2. **Personalized Marketing**: Provide personalized marketing campaigns and product recommendations to increase engagement and loyalty.
3. **Luxury Experience**: Offer luxury experiences, such as exclusive events and personalized customer service, to increase customer satisfaction.

### Cluster 3: "Mainstream Customers"
1. **Targeted Marketing**: Launch targeted marketing campaigns to increase engagement and loyalty among Mainstream Customers.
2. **Product Bundles**: Offer product bundles and discounts to increase average spend and frequency.
3. **Customer Feedback**: Collect customer feedback to improve products and services and increase customer satisfaction.

# Power BI Visualization Guide
To build interactive dashboards, follow these steps:
1. **Create a customer segments table**: Create a table with customer segment information, including cluster assignment and demographic data.
2. **Join customer segments to customer data**: Join the customer segments table to the customer data table using the customer ID.
3. **Join customer data to transaction data**: Join the customer data table to the transaction data table using the customer ID.
4. **Create visualizations**: Create visualizations, such as bar charts and scatter plots, to display customer segment information and transaction data.
5. **Use filters and slicers**: Use filters and slicers to enable interactive filtering and exploration of the data.
Example schema relationships:
```sql
customer_segments
  JOIN customers ON customer_segments.customer_id = customers.customer_id
  JOIN transactions ON customers.customer_id = transactions.customer_id
```
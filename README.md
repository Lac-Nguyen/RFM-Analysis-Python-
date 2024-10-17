# RFM Analysis

This project aims to analysis segment of customer bases on RFM Model, so that Marketing team can deploy each marketing program suitable for each customer group.
## 1. Introduction
### 1.1. Business current situation
SuperStore is a global retail company, which means it has a large customer base. On the occasion of Christmas and the New Year, the Marketing Department wants to run marketing campaigns to show appreciation to customers who have supported the company over time, as well as to target potential customers who could become loyal clients.

However, the Marketing Department has not yet been able to segment this year's customers due to the large dataset, making it impossible to process manually as in previous years. Therefore, they are requesting the Data Analysis Department to assist in developing a classification model to segment each customer for implementing tailored marketing programs for each customer group.

The Marketing Director has also suggested using the RFM model; however, in the past, when the company was smaller, the team could manually calculate and classify customers using Excel. Currently, the volume of data is too large, so they hope the Data Department can build a workflow to evaluate segmentation using Python programming.

### 1.2. RFM segmentation
The “RFM” in RFM analysis stands for recency, frequency and monetary value.
- Recency: measures how recently a customer has made a purchase.
- Frequency: measures how often a customer has made purchases.
- Monetary Value: measures the total amount of money a customer has spent on purchases. RFM is used to identify and categorize customers based on their purchasing behavior and how recently and frequently they have made purchases, as well as the monetary value of those purchases.

## 2. Requirements
The Marketing Department needs to classify customer segments in order to deploy suitable marketing programs for each group. The Marketing Director also proposed a plan to use the RFM model in Python to segment customers, allowing for the launch of marketing campaigns that thank customers for their support over time, as well as target potential customers to become loyal clients.

Additionally, suggestions for the Marketing and Sales teams regarding the company's retail model: which of the three R, F, and M indicators should be prioritized?

## 3. Data exploration and insights 
(The Python code file is attached above)
### Recency
![image](https://github.com/user-attachments/assets/fe79904e-4fde-40b9-ae12-a527af23c746)

Recency primarily falls within the range of 0-200, indicating that the most recent transactions occurred within the last 200 days, after which the frequency decreases. It can be inferred that, within this 200-day period, a significant number of existing customers return to make purchases, possibly along with new customers. After 200 days, the number of returning customers drops significantly, and as time goes on, fewer customers return to make purchases. This allows for the identification of customer segments.

### Frequency
![image](https://github.com/user-attachments/assets/3ab5436e-65b8-4f29-8893-c3cf309c1aff)

Frequency ranges from 2 to 10, with the highest occurrence at 6 orders, gradually decreasing to 12. Based on this, we can hypothesize that the number of orders reflects the level of customer engagement with the business through promotional and PR campaigns. When customers make frequent purchases, it indicates that these marketing efforts are effective, strengthening the relationship between the business and its customers. Additionally, this analysis helps identify customer segments: those with order frequencies between 4 and 8 are typically loyal and engaged customers. This insight allows for the development of appropriate customer incentive policies, enhancing interactions between customers and the business, ultimately leading to increased revenue.

### Monetary
![image](https://github.com/user-attachments/assets/c5415d3d-974c-4451-87d0-1c1f35479c07)

Monetary values primarily range from 0 to 5000, with a peak at 1000, indicating the purchasing power of customers. Products priced within the 0-5000 range are popular, suggesting that promotional campaigns, discounts, and offers can effectively drive sales for both high-demand and slow-moving inventory. Once customers experience the quality of discounted items, they are more likely to trust and invest in these products when the discounts are no longer available. This strategy can ultimately lead to increased revenue from other product lines within the company.

![image](https://github.com/user-attachments/assets/b46657a6-e546-4fc0-9d91-3b2473052194)
- The most recent purchase segments are Champions (28.5 days) and Promising (35.3 days). 
- The segments that haven’t made purchases in a long time are Cannot Lose Them (496.5 days) and Lost Customers (558.0 days).
- The time since the last purchase shows minimal difference between the Champions and Loyal segments, indicating that these are the segments to focus on. However, from the About to Sleep segment onward, the gap in purchase recency widens significantly.
  
![image](https://github.com/user-attachments/assets/70fb2ab7-29d0-451b-bb20-21f7928bf572)
- The most frequent purchasing segments are Champions (9.8 purchases), Loyal (8.2 purchases), and At Risk (7.3 purchases).
- The segments with the fewest purchases are New Customers (3.4 purchases) and Lost Customers (3.0 purchases).
- The difference in frequency among the segments is gradually decreasing and is not as pronounced as in recency (which nearly drops by one purchase per level). Notably, the At Risk segment ranks in the top three for purchase frequency, which is unusual given that its recency places it among those who haven’t purchased in a long time. This suggests that the At Risk segment tends to make purchases during special occasions, such as major holidays (Valentine's Day) or significant sales events (Black Friday).
  
![image](https://github.com/user-attachments/assets/a97cc79e-ff37-4e59-aaaf-6a88a484f462)

The segment with the highest average spending is Champions ($5,381.6), followed by Loyal customers ($4,365.8). In contrast, the segments with the lowest average spending are New Customers ($672.1) and Lost Customers ($653.8). Loyal customers, who have a strong relationship with the business, tend to spend the most on products because they trust the company. On the other hand, New Customers may be hesitant to invest in the company's products, likely due to a lack of experience with them, resulting in insufficient trust. Additionally, some other segments may have lower demand for the company's offerings.

However, this analysis of average spending is intended to identify trends among customer segments and may not fully capture the complete picture. The At Risk segment is presumed to have a tendency to make purchases during special occasions, which could lead them to spend the most overall across all segments.
## 4. Conclusion and suggestions
### Percentage of customer segments based on the total number of customers
![image](https://github.com/user-attachments/assets/feba753c-7e0b-4747-bfa4-70a52ee572cd)
### Percentage of customer segments based on the total revenue
![image](https://github.com/user-attachments/assets/d9e5146f-d97a-4a3c-b59b-dbd628443478)
### 1. Champions Segment
This segment represents 8.98% of the total customer base and accounts for 18.05% of total revenue. They have the highest purchase frequency, rank first in recency, and also have the highest average spending. This group is the most important for the company, so it should receive the best customer care services, along with various offers and gift vouchers. Regularly running marketing campaigns for new products aimed at this segment can help increase their purchasing activity.
### 2. Loyal and Potential Loyalist Segments
The Loyal segment comprises 7.84% of the total customers and contributes 12.79% to total revenue. They rank second in purchase frequency, with an average recency of 60 days and the second highest average spending. The Potential Loyalist segment accounts for 14.29% of the total customers and contributes 9.02% to total revenue, with an average recency of 45 days, a relatively high purchase frequency (7.1 times), and average spending positioned in the middle of the segments.

Both of these groups are also very important. Loyal customers have the potential to develop into Champions, while Potential Loyalists can become Loyal customers. Therefore, providing excellent customer care for these segments is essential, making them feel special and valued by the company. This can enhance interaction and trust in the business. Once customer trust is established, the company can begin to propose higher-value products and offer promotions tailored for them.
### 3. New Customers and Promising Segments
The New Customers segment accounts for 7.71% of the total customer base and contributes 1.94% to total revenue, with an average recency of 41.5 days. This group has the second lowest purchase frequency and average spending. The Promising segment comprises 7.96% of the total customers and contributes 10.62% to total revenue, with a second-highest average recency of 35.3 days. However, this group exhibits relatively low purchase frequency and average spending.

Both segments represent customers who are just beginning to experience the company's products. Their trust in the products is not yet strong, so it is crucial to provide attentive customer service and maintain more frequent interactions. Offering attractive promotions and providing detailed product descriptions can help foster openness. Encouraging purchases through initiatives like "the more you buy, the more you save" and asking customers to share their experiences can also attract new customers.
### 4. Need Attention and About to Sleep Segments
The Need Attention segment represents 9.1% of the total customer base and accounts for 12.26% of total revenue, with an average recency of 50.1 days. This group has relatively moderate purchase frequency and average spending. The About to Sleep segment makes up 5.56% of the total customers and contributes 2.24% to total revenue, with an average recency of 135.2 days. Their purchase frequency is average, but their average spending is somewhat low.

=> These two groups have not made recent purchases, so the business should investigate the reasons behind this. It could be due to product quality, service issues, or pricing. Additionally, launching a campaign like "Welcome Back" with significant discounts on previously purchased products can encourage these customers to return, while also promoting the exploration of other product offerings.
### 5. At Risk and Cannot Lose Them Segments
The At Risk segment comprises 12.14% of the total customer base and accounts for 18.24% of total revenue, with an average recency of 259 days. This group ranks in the top three for purchase frequency, making an average of 7.3 purchases, and their average spending is also among the top four. In contrast, the Cannot Lose Them segment accounts for 4.55% of the total customers and contributes 7.1% to total revenue, with an average recency of 495 days. This segment has relatively low purchase frequency, but their average spending is in the top three.

Both segments show a tendency to make purchases based on need. The At Risk customers are willing to spend (contributing the highest total revenue) and make multiple purchases, but their recent purchase activity suggests they typically buy during specific occasions throughout the year. To capitalize on this, the business should identify when the At Risk segment tends to shop and launch targeted marketing campaigns and promotions during those times, particularly around special events.

The Cannot Lose Them segment appears to purchase only when they need a specific product, showing less interest in other offerings. Understanding the categories and sub-categories they frequently buy from can help suggest additional similar products, potentially stimulating customer demand.
### 6. Hybernating and Lost Customers Segments
The Hybernating segment accounts for 11.38% of the total customer base and contributes 5.19% to total revenue, with an average recency of 190 days. Both their purchase frequency and average spending are relatively moderate. In contrast, the Lost Customers segment represents 10.49% of the total customers but only 2.56% of total revenue, with the lowest average recency of 558 days. This group also ranks last in both purchase frequency and average spending.

These two segments seem to indicate a loss of connection with the business, as they contribute minimally to revenue and purchasing activity. However, the substantial number of customers in these segments presents an opportunity. Re-engaging with them could unveil a valuable resource. To increase interaction with these groups, the company should leverage social media, send targeted emails, and implement programs like "Customer Appreciation for Long-Time Clients" to rekindle their interest and create demand.

### Suggestions
In the RFM metrics, the most important indicator for the marketing team is Recency (R). Recency reflects the level of interaction between customers and the business; a high Recency indicates that customers are returning to use the company’s products frequently. This suggests that marketing and PR campaigns are effective and that the product quality has gained credibility. The primary goal of running marketing campaigns is to increase revenue and brand awareness, as well as the company's presence among customers. Therefore, a high Recency can lead to increased Frequency (F) and Monetary (M) values, depending on the product's value.

For the sales team, the most crucial indicator is Frequency (F). Frequency indicates customer satisfaction with the company’s products; high-quality products lead to frequent and multiple purchases. Segments with high Frequency also tend to exhibit high Monetary values, enhancing customer satisfaction with the products. As a result, customers buy more, which ultimately increases revenue.




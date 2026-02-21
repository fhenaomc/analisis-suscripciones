# Exploratory Analysis 


### product_info Table

- **Total products :** 2
- **Billing cycles :** Annual or monthly subscription
- **Prices :** 
	- The monthly subscription ($125) is 25% more expensive than the annual subscription ($1,200) on a yearly basis.
	- The annual subscription becomes more cost-effective for customers who remain subscribed for more than 10 months.	


### customer_cases Table

- **Total customer cases :** 330512
- **Distinct customer with cases :** 258660 
- **Case distribution :**
	- 200985 support cases
	- 129527 sign up cases
- **Case date range:** From 2017-01-01 10:32:03 to 2022-01-01 06:32:53
- No duplicate case_id values were found


### customer_info Table

- **Total customers:** 508932
	- 309930 male customers
	- 199002 female customers
- **Ages range :** 21 to 78 years


### customer_product Table

- **Total customers :** 508932
- No duplicate customer_id values were found
- The total number of customers matches the customer_info table
- Each customer is associated with exactly one product
- No records were found where cancel_date_time precedes signup_date_time
- **Customer status: **
	- 112485 churned customers
	- 396447 active customers
	
Dataset appears structurally consistent in all four tables.
title:: Payments 101 for a Developer (highlights)
author:: [[manojr13]]
full-title:: "Payments 101 for a Developer"
category:: #articles
url:: https://github.com/juspay/hyperswitch/wiki/Payments-101-for-a-Developer

- Highlights first synced by [[Readwise]] [[May 1st, 2023]]
	- All transactions are aggregated under the Payment Processors' master MID, and the merchants will not have to enter into any contractual relationship with a bank. `Stripe`, `Adyen` and `Paypal` are examples of Payment Processors. ([View Highlight](https://read.readwise.io/read/01gz2fqcacggx2ak3atwfj6syy))
	- `Payment card industry` (PCI) compliance is mandated by card companies to help ensure the security of card transactions in the payments industry. Any merchant that wants to process, store or transmit credit card data must be PCI compliant, according to the PCI Compliance Security Standard Council. ([View Highlight](https://read.readwise.io/read/01gz2fqgsz8r9ybhhfjc7dydry))
	- Payment Status validation
	  
	  Upon completion of the payment, the status of the payment shall be updated, and the corresponding success/ failure page should be displayed to the customer. Generally, there are three means by which the status is validated.
	  
	  •   Payment status API: Query the payment status through a server API using the respective payment identifier.
	    
	  •   Redirection: Upon completion of payment, the customer will get redirected to your domain with the payment status in the query params. Most processors provide the option of configuring such a URL through the dashboard interface or providing the URL as a parameter in the server API mentioned in Step 1.
	    
	  •   Webhooks: Webhooks are automatic server-to-server notifications triggered from the payment processor's server to your server every time the payment status updates. You can configure the webhook endpoint in the dashboard interface of the payment processor and subscribe for webhooks events you wish to receive. ([View Highlight](https://read.readwise.io/read/01gz2fqrf7cfbdhanrz4b0y4y5))
	- In general are three kinds of causes for disputes:
	  
	  •   **Merchant error** may occur due to customer dissatisfaction with the product, shipping issues, or failure to cancel product subscriptions at the right time.
	    
	  •   **Criminal fraud** may occur due to a customer's stolen or compromised card details, leading to illegitimate purchases.
	    
	  •   **Friendly fraud** happens when a cardholder misuses the chargeback process, either as an intentional attempt to get something for free or an innocent misunderstanding. Delayed refunds or poor response from customer service could also result in friendly fraud. ([View Highlight](https://read.readwise.io/read/01gz2fqxm1y0g3fjnrvpyyh0jw))
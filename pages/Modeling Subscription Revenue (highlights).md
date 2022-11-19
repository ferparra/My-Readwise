title:: Modeling Subscription Revenue (highlights)
author:: [[blog.getdbt.com]]
full-title:: "Modeling Subscription Revenue"
category:: #articles
url:: https://blog.getdbt.com/modeling-subscription-revenue/

- Highlights first synced by [[Readwise]] [[Nov 18th, 2022]]
	- If you’re a data analyst at a SaaS company or an ecommerce business with a subscription component, it is inevitable that you will be asked to analyze metrics like churn, upgrades, and downgrades.
	- Your business logic is codified: Every business is unique, and the way your business defines a churn is likely to be subtly different to another business. By building a data model that contains this business logic, you’re able to ensure everyone in your business is using the same definition.
	- Your assumptions about your data model can be tested: By building data models in dbt, you can explicitly list and then test any assumptions you’re making about your data. For example, if your back-end team tells you that a customer can’t have two active subscriptions at once, it’s a good idea to add a test to validate that (here’s an example).
	- new: the customer is a new customer that has not had a previous subscriptionchurn: last month the customer paid for a subscription, but this month is not. A customer can churn many timesupgrade: the customer has increased their usage and is now paying you more money per monthdowngrade: the customer has decreased their usage and is now paying you less money per monthreactivation: a previously churned customer has started subscribing again
	- What is your business’ tolerance for numbers that don’t perfectly match with financial reports?Does your business allow users to pause subscriptions? Should this be tracked differently than a churn?What is your base unit of measure (i.e. customer, account, product)?Are there any add-on costs that are useful to add as an attribute on this table?How should partial months be handled?Do all subscriptions get charged on the same day, or do they get charged on a different day for each customer? If the latter, what is the business rule for the month that the revenue gets recognized in?
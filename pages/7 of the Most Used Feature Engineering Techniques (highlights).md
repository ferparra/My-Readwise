title:: 7 of the Most Used Feature Engineering Techniques (highlights)
author:: [[Dominik Polzer]]
full-title:: "7 of the Most Used Feature Engineering Techniques"
category:: #articles
url:: https://towardsdatascience.com/7-of-the-most-used-feature-engineering-techniques-bcc50f48474d
document_note:: Feature engineering is a process used to transform and prepare data for machine learning algorithms. There are several techniques used for this, such as encoding and vectorizing categorical data, binning or bucketizing for both numerical and categorical data, and reducing dimensionality with hashing and principal component analysis (PCA). Examples of these techniques are provided, such as one-hot encoding using Scikit-learn and Tensorflow, and adjusting the parameter lambda (λ) to tailor the transformation of the data. Sources and further reading are also provided.
tags:: #[[feature engineering]] #[[machine learning]] 
![](https://readwise-assets.s3.amazonaws.com/media/uploaded_book_covers/profile_5318/1vaXzV9kTLdiVTcoJ94hmXw.png)

- Highlights first synced by [[Readwise]] [[Mar 24th, 2023]]
	- Feature engineering describes the process of formulating relevant features that describe the underlying data science problem as accurately as possible and make it possible for algorithms to understand and learn patterns. In other words: ([View Highlight](https://read.readwise.io/read/01gw9afdzb9q2279g7c5cqf5jp))
	- What Forbes magazine considers as “cleaning and organizing” is usually broken down into two to three subcategories in the ML pipeline (I have highlighted them with a yellow background in the image above):
	  
	  **(1) Data (Pre-)Processing:** The initial preparation of the data — for example, smoothing a signal, dealing with outliers, etc.
	  
	  (2) **Feature engineering:** Defining input features for our model — e.g., by converting an (acoustic) signal to the frequency domain using the fast Fourier transform (FFT) allows us to extract crucial information from the raw signal.
	  
	  (3) **Feature Selection:** Selection of features that have a significant impact on the target variable. By selecting the important features and thus reducing the dimensionality, we can significantly reduce the modeling costs and increase the robustness and performance of the model. ([View Highlight](https://read.readwise.io/read/01gw30ph2eqmew858p8f3q5hqp))
	- **(1) Data (Pre-)Processing:** The initial preparation of the data — for example, smoothing a signal, dealing with outliers, etc. ([View Highlight](https://read.readwise.io/read/01gw9afkyvar7y7ze0cgbyg3jw))
	- (2) **Feature engineering:** Defining input features for our model — e.g., by converting an (acoustic) signal to the frequency domain using the fast Fourier transform (FFT) allows us to extract crucial information from the raw signal. ([View Highlight](https://read.readwise.io/read/01gw9afmv9dwr1b4c2v9av19na))
	- (3) **Feature Selection:** Selection of features that have a significant impact on the target variable. By selecting the important features and thus reducing the dimensionality, we can significantly reduce the modeling costs and increase the robustness and performance of the model. ([View Highlight](https://read.readwise.io/read/01gw9afrayck9jx1r2v5qqec71))
	- ***In the manufacturing sector***, equipping production facilities with comprehensive sensor technology and connecting them to databases is expensive. As a result, many plants do not yet collect data at all. Even when machines are able to collect and store data, they are rarely connected to a central data lake. ([View Highlight](https://read.readwise.io/read/01gw30ptw8amavk17313rf10pj))
	- I***n the supply chain context***, every company has only a certain number of orders that it processes every day. So if we want to predict the demand for a product that is in very irregular demand, we sometimes have only a few data points available. ([View Highlight](https://read.readwise.io/read/01gw30py4fqvsdb4azv9749j0m))
	- **Label encoding** involves assigning a numeric value to each categorical value. This can be effective if there is an inherent order to the categorical values, such as grades from A to F, which can be encoded as numeric values from 1 to 5 (or 6). However, if there is no inherent order to the categorical values, label encoding may not be the best approach. ([View Highlight](https://read.readwise.io/read/01gw30rhfve0hm7nzs3j6yymad))
	- Alternatively, you can use **One-hot encoding** to transform categorical values into numerical values. In one-hot encoding, the column of categorical values is split into several new columns, one for each unique categorical value. ([View Highlight](https://read.readwise.io/read/01gw30rmarqv9h28r2bp4qjkk8))
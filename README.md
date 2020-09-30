# Recommendations-with-IBM

Analyze the interactions that users have with articles on the [IBM Watson Studio platform](https://www.ibm.com/cloud/watson-studio), and make recommendations to them about new articles they might like.

## 1. Data Exploration

Explore the data to understand the number of users, articles, and information about the interactions that take place.

Used the dictionary and necessary method to provide insights into the descriptive statistics of the data.

## 2. Rank Based Recommendations

Pulls top articles based on the article's popularity. Here popularity is measured by the number of interactions it has with users. 


## 3. User-User Based Collaborative Filtering

For a given user, finds the most similar users to that user. Then we recommende the articles liked by those similar users but are not yet seen by the given user.

The similarities between the users are measured in terms of the articles they interacted with. The more articles they have read in common, the higher the similarities. 

In order to compute the similarities, we need to create a matrix with users on the rows and articles on the columns. There is a 1 if a user-article interacted with one another and a zero otherwise. The user similarity is then computed by taking the dot product of the rows associated with the users.

If there are two users have the same similarities, we further rank them by users who have the most article interactions.

The recommended articles are ranked by articles with the most interactions.

For new users, which will not be able to receive recommendations using our user-user based collaborative filtering method, we make recommendations by Rank-based recommendations, 

## 4. Content Based Recommendations

I used NLP to find the articles that are most similar to the given article.
I transformed the article titles into TF-IDF vectors and then compute the cosine similarity between rows. The content based recommendation will return the articles with the highest similarity with the given article.


## 5. Matrix Factorization

Split the user-item matrix into training and testing segments and performed SVD on user-item matrix. 

Perform assessment of the predicted vs. the actual values.



!(https://github.com/JPL13/Recommendations-with-IBM)

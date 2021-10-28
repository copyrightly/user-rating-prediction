In this model, we use matrix factorization to predict user ratings.

In the first part, we use k-means clustering to divide users into 3 clusters and then we train our models on each cluster.

For each cluster, we first use users with rating record to find users features and product features under the assumption that rating matrix R=UP. Then we can use this factorization to predict missing ratings for the first 3000 users. Moreover, we find the connection between user history and user features under the assumption that U can be factorized into U=HW, where H is user history.

For the remaining 1500 users without any rating record, we use the matrix W computed above and their history to find their user features. Then the product of this user feature matrix and product feature matrix gives the predicted ratings.

To reproduce the result, you can simply run each cell in the Jupiter notebook sequentially.
# KNN_imputer_from_scratch


-Here I have created KNN and KNN_imputer from scratch using python.
-Both knn and weighted Knn imputer function take input dataframe having nan and then outputs the imputed values in a dataframe based on KNN approach.
-Here we can also output k nearest neighbour for the point we want by slightly changing the code.

Explanation of results

Here the weighted knn with k=5 has performed well for both original and scaled data followed by
Knn.
These is due to the fact that as we increase number k the results are more generalised and not skewed towards particular points.So it might be possible if we increase k more than 5 we may get even good results comparatively, but after certain value of k results may not be consistent.

Results across different features:
As we have 13 different features ,but the mse is different for different features ,this is due to the distribution of particular feature .If particular feature is ranging from 1 to 10 and another feature is ranging from 1 to 100 , second feature will show more error because it has high range. There is problem with the error metric we used
MSE has the problem of interpretability ,i.e as we know less the value of error the better the model is but 0 is least value that can be possible but what is the upper limit of error.That is where problem is,upper limit of error is not defined.
That means  mse error of feature 1 is 10
And mse error of feature 2 is 15.
But we cant say error  on feature 1 is high because as said feature might have more range compared to feature 2.Feature 1 has more variance than feature 2.
But this problem can be solved using scaling that is why we have similar mse in scaled data because we are removing high variance among features.

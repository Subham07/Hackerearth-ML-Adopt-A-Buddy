# Hackerearth-ML-Adopt-A-Buddy
My approach for solving the Hackerearth ML Adopt A Buddy challenge. (Top 4%)

# Problem Description: 
https://www.hackerearth.com/challenges/competitive/hackerearth-machine-learning-challenge-pet-adoption/machine-learning/pet-adoption-9-5838c75b/

We have been given training and testing dataset which has columns like the Pet_Id , Condition , Color , Issue and Listing Date. The target variables are the breed_category and pet_category which we need to predict

As there are two classes , the approach taken is training two models for each classes and then testing seperately and appending the final result.

All the code with explanations are given in the .ipynb file.

I have also given training and testing data for reference.

Notebook was created in Google Colab

# Pre-processing

During pre-processing, following things were checked and rectified according
* Calculating columns with NAN values and replacing with a meaningful value
* Measuring the Skewness in Distibutions of value and normalizing it

# Feature-Engineering

Features were added in the following way:
* For the two date-time columns, difference in days were calculated and added to the data as a new feature
* Length and Height, were divided into Small-Medium-Large category according to the values in respective columns
* Absolute value of difference in days was considered as the difference was negative in some cases
* Length was in m so it was converted into cm (same as units for Height) and then ratio of both of them was used as another feature.

# Training and Testing
XGboost gave the best performance. RandomforestClassifier, LGBM and Catboost were also used. Parameter tuning was also done for Xgboost.

# Final Submission
Final submission ranked me under top 100 as of now (39th) with average F1 Score of 91.06 (public leaderboard). Topper's score is 91.5. Point to note is that my score was 90.83 but the performance improved after final two points in the Feature engineering category were considered (given above)

# If you like it, please give stars and comment for feedback. Thanks

# Restaurant-Rating-Prediction-EDA
Predict the rating of the restaurant on TripAdvisor

# Summary:
* Analysis and preparation of dataset modeling with information on restaurants from TripAdvisor were carried out.
* The missing values in the 'Number of Reviews', 'Price Range' and 'Cuisine Style' features were filled in.
* At the same time, new features 'isnan' were created with information about the absence of data.
* The categorical feature 'City' was encoded using the get_dummies function.
* Created a new attribute 'Population' (information about the population of cities entered manually in the form of a dictionary).
* Based on this, new relative features were created: 'Review to Population' (the ratio of the number of reviews to the population) and 'Rel Rank to Population'.
* Order sign 'Price Range' - 3 gradations - was replaced by consecutive numbers 1,2,3. Most restaurants are in the middle price range.
* Categorical attribute 'Cuisine Style': there are 125 unique cuisines in the dataset.
* The most common - vegetarian, European, other (this includes all the gaps on the basis of 'Cuisine Style'),mediterranean and italian).
* Based on 'Cuisine Style', features were created with the number of cuisines in the restaurant, as well as two features 'Cusine Style 1' and 'Cusine Style 2'.
* They include the first two and the next three of the most popular cuisines.
* According to information published by Tripadvisor, the presence of recent reviews plays a significant role in the ranking of establishments.
* So the lack of reviews can lead to a drop in the rating relative to those institutions where they were left recently.
* Based on the 'Reviews' feature, the dates of the reviews were extracted and a feature was created with the difference in days between two reviews ('Review Update').
* 'New Review' reflects the relevance (relative to the timeline) of the establishment's reviews. That is, which establishments have the most recent reviews.
* In fact, these features did not make the greatest contribution to improving the accuracy of the simulation.
* A new attribute 'Relative Ranking' has been created - the ratio of the rank of a restaurant to the number of restaurants in this city according to the dataset.
* Normalization of the feature "Ranking" relative to the maximum value in the dataset makes the greatest contribution to improving the accuracy of modeling.
* The correlation matrix showed no multicollinearity, so all features were left for further use in the ML model.
* All iterations kept MAE close to 0.20000.
* But rounding the simulation results (to 0.5, like the 'Rating' step in the original dataset) was able to reduce the absolute error.
* As a result, we managed to get MAE=0.1691875. This is already significantly less than the MAE from the baseline notebook.

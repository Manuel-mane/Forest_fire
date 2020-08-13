# Forest_fire

### Personal Notes 
This is my first personal project in ML-Data Science.
This is a beginner level project where I put in practice some of the concepts learnt in the last months about the development of an end-to-end ML project. This is a regression model, where I develop some EDA (Exploratory Data Analysis) to draw valuable information from my data and then apply 4 different regression models to test which one gives me better results. Obviously, I am aware the code and processing need a lot of work, and I am really exciting in working forward to improve it with the development of future projects.

## Description of the project

Using a dataset from UCI, I statistically analyzed the dataset and apply different ML to obtain the most effective one.

The objective of this project was to consolidate statistical and analytical skills as well as obtaining practical experience by 
using regression models to find the best possible model to predict the affected area for forest fire in a region of Portugal by
using this dataset.

The results were not the best in the first two approaches, mainly due for the characteristics of the dataset and the lack of data.

### Dataset and Modeling approaches:

Our dataset contained many outliers that were critical for the real use, so they could not be all removed. However, using a different
approach, we could a get a better solution for the prediction of the affected area from forest fire in Portugal. These are the different
approaches:

1. First, Decision Tree Regressor model gives us the best result with Mean Absolute Error around 5 when the most critical outliers
were removed.

2. Our target (area [ha]) contained many zeros for different features, that affected the proper modeling of our data because it skewed the
distribution of our dataset. Because of this, I set a different dataset where only the features that led to the ocurrence of forest
fire (area > 0). This dataset is called forest_fire_affected_areas. Building a prediction model with this dataset will predict the
area (ha) that could be affected when a fire breaks up given the different features. Again, the results were not the best mainly
due to most of the area data where below the 15ha and around 10 % were above up to 278ha which it mas the maximum, so again our 
dataset was skewed. We could not remove these outliers because there were critical in the real prediction. We need to know when the
conditions are set for a possible forest fire that can cover such a large area. For this reason, I think I can build a classification
prediction model able to predict when a forest fire is up to cover areas larger than 50ha and lower than it.

3. This third approach divides the target area from low affected and high affected areas. The goal of this approach is to be able
of getting a better prediction when a forest fire can cover larger areas (threshold point still to decide) and low areas. Even 
though the exact number can not well predicted due the complexity of the dataset or the lack of information, this approach is able
to give an alarm when conditions are set for a forest fire to cover large areas with a higher accuracy than prior approaches.

4. Last but no least, the four approach is a classification model that predict whether the features can lead to forest fire. This approach is not developped in this notebook due this one is focused in regression models. But the idea would be to divide the area by 0 and bigger than 0, so in this case I will predict whether the features are favorable for a forest fire to break. Again, this approach should give me a better accuracy than the first 2 approach.



# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Hawa Desai

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I had to first correctly make sure that the .csv files were formatted correctly, and I also had to make sure I was ignoring the correct columns. I did not ignore the casual and registered columns at first and realized that I could not predict on the test data set, which therefore affected my scores because I was predicting on the train dataset. When doing the second model run, I also struggled at first to fix my .csv folder because I had somehow created a second date column and then submitted a .csv with three columns rather than the two I needed. 

### What was the top ranked model that performed?
The top ranked model was my last model.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
My EDA found that the minimum value in the count column was 2.921356, and once I added an additional feature the minimum was 3.344096. I also used histograms and there was not much difference in the histograms except for the hour histogram which the values are going up and down once I added the feature. I added the additional feature by adding an hour column to the training data by seperating the column from the datetime object.

### How much better did your model preform after adding additional features and why do you think that is?
My model performed much better by dropping the score from an approximate 1.8 to around a 0.6, and it's possible that because the model was trained with a new feature that the score was better and the training performed slightly better.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
My model performed better after trying different hyperparameters, by dropping the already improved score of approxiamtely 0.6 to 0.4. 

### If you were given more time with this dataset, where do you think you would spend more time?
I would spend more time exploring the data and trying out different features and how they impact the model and my score.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|default|default|600 seconds|1.80555|
|add_features|default|hour added|600 seconds|0.63768|
|hpo|default|light hyperparemeter added|600 seconds|0.46047|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.
<img width="575" alt="first_graph" src="https://github.com/hawaDprograms/udacityproje/assets/93603120/b4ade2e3-dc32-4cea-8df2-e5e02de909b0">

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

<img width="575" alt="Screenshot 2023-06-04 at 1 02 12 PM" src="https://github.com/hawaDprograms/udacityproje/assets/93603120/17a2f1a5-2778-44da-8750-0960a206b5ab">

## Summary
The time spent training the model did not change, but the hyperparameter changed and there was a feature added. After adding a feature, my score improved and after adding in a hyperparameter my score improved even more.

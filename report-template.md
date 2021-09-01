# Report: Predict Bike Sharing Demand with AutoGluon Solution
Akíntúndé `theyorubayesian` Ọládípọ̀

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
Some of the predictions were negative resulting in an error when they were submitted for evaluation. It was necessary to clip them to 0 as follows:
```python
predictions.loc[predictions < 0] = 0
```

### What was the top ranked model that performed?
TODO: Add your explanation

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The distribution for `windspeed` close to Poisson. `Temperature` and `Humidity` however had normal distributions.
Most of the data was from working days. Three additional features were added: `hour`, `day`, and `month` created from the `datetime` column.

### How much better did your model preform after adding additional features and why do you think that is?
TODO: Add your explanation

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: Add your explanation

### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|?|?|?|?|
|add_features|?|?|?|?|
|hpo|?|?|?|?|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![model_test_score.png](img/model_test_score.png)

## Summary
TODO: Add your explanation

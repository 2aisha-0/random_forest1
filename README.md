# Random Forest

ML assignment 3

i used random forest to predict the fitness class of a person (A, B, C, D). A is the best and D is the worst

## Dataset
Body Performance Data from kaggle (13393 rows)

same data as the logistic regression assignment but this time i used all 4 classes not binary

## Notebook
- random_forest.ipynb

## Steps
1. load the data
2. remove the duplicate and the wrong values (like blood pressure = 0)
3. change gender to 0/1
4. train test split (80/20), no scaling because random forest doesnt need it
5. random forest with default values
6. gini vs entropy
7. trying different max_depth
8. hyperparameter tuning with GridSearchCV
9. accuracy, precision, recall, f1, classification report and confusion matrix
10. feature importance

## Results (test set)
| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| Default | 0.724 | - | - | - |
| After tuning | 0.734 | 0.739 | 0.735 | 0.734 |

best params: n_estimators = 200, max_depth = 20, max_features = sqrt, min_samples_split = 2

the default model was overfitting (train accuracy = 1). class A and D were the easiest to predict and B and C were the hardest because they are in the middle. the most important feature was sit and bend forward

## How to run
open the notebook on kaggle, add the Body Performance Data dataset and run all

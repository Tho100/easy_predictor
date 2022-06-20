# Easy Predictor 

Perform regression prediction on small Excel dataset in one line!

# Side Note

Currently only two columns are allowed be use on the prediction (Independent & Dependent variable).

## Instruction

1. Linear Regression Prediction

```python
from easy_predictor import linear 

dataset = "path_to_excel_file"
linear.predict(dataset,column_x,column_y,value: int)
```
2. Text Classification Prediction

```python
from easy_predictor import classification

dataset = "path_to_excel_file"
classification.predict(dataset,column_x,column_y,value: str)
```

## Result (Linear)
```python
dataset = "C:\\users\\USER\\Documents\\Dataset_file\\scores_pred.xlsx"
predict(dataset,'Study Hour','Scores',15)
OUTPUT: [[62.]]
```

## Result (Classification)
```python
dataset = "C:\\users\\USER\\Documents\\Dataset_file\\sentiment_tf.xlsx"
predict(dataset,'Text','Sentiment','Hatred')

OUTPUT: ['NEGATIVE']
```

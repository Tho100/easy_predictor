![Screenshot_10](https://user-images.githubusercontent.com/64541739/174754962-952e3e72-0b2c-4ae6-987d-9f46c965e5c4.png)


Perform regression/classifcation prediction on small Excel dataset in one line!

# Side Note

Currently only two columns are allowed be use on the prediction (Independent & Dependent variable).

## Instruction

0. Installation

```
pip install easy-predictor
```

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

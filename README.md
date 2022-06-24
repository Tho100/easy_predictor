![Screenshot_10](https://user-images.githubusercontent.com/64541739/174754962-952e3e72-0b2c-4ae6-987d-9f46c965e5c4.png)


Perform regression/classifcation prediction on small Excel dataset in one line!

## Instruction

0. Installation

```
pip install easy-predictor
```

1. Linear Regression Prediction

```python
from easy_predictor import linear 

dataset = "path_to_excel_file"
linear.predict(dataset,dtype: str,[column_x],value: int,column_y)
```
2. Text Classification Prediction

```python
from easy_predictor import classification

dataset = "path_to_excel_file"
classification.predict(dataset,dtype: str,column_x: list[str],value: list[str],column_y)
```

3. Visualize Excel Data In Tabular Form

```python
from easy_prediction import table 

dataset = "path_to_excel_file"
table.tabulator(dataset,dtype: str,columns=list[str])
```

## Example (Linear Regression)
```python
from easy_predictor import linear

dataset = "C:\\users\\USER\\Documents\\Dataset_file\\scores_pred.xlsx"
linear.predict(dataset,'xlsx,'Study Hour','Scores',15)
OUTPUT: [[62.]]
```

## Example (Classification)
```python
from easy_predictor import classification

dataset = "C:\\users\\USER\\Documents\\Dataset_file\\sentiment_tf.xlsx"
classification.predict(dataset,'xlsx,'Text','Sentiment','Hatred')

OUTPUT: ['NEGATIVE']
```

## Example (Data Visualization)
```python
from easy_predictor import table 

dataset = "C:\\users\\USER\\Documents\\Dataset_file\\scores_pred.xlsx"
table.tabulator(dataset,'xlsx',columns=['Hour Study','Scores'])

OUTPUT:       

     Hour Study    Scores
--  ------------  --------
 0           2          10
 1           2.5        12
 2           3          14
 3           3.5        16
 4           4          18
 5           4.5        20

```

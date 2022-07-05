![Screenshot_10](https://user-images.githubusercontent.com/64541739/174754962-952e3e72-0b2c-4ae6-987d-9f46c965e5c4.png)


Perform regression/classifcation prediction on Excel dataset.

## Instruction

0. Installation

```
pip install easy-predictor
```

1. Linear Regression Prediction

```python
from easy_predictor import linear 

dataset = "path_to_excel_file"
model = linear.linear_regression()
model.predict(dataset,data_type: str,column_x: list[str],value: list[int],column_y: str)
```
2. Text Classification Prediction

```python
from easy_predictor import classification

dataset = "path_to_excel_file"
model = classification.classification()
model.predict(dataset,data_type: str,column_x: list[str],value: list[int],column_y: str)

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
from easy_predictor import linear

dataset = "C:\\users\\USER\\Documents\\Dataset_file\\scores_pred.xlsx"
model = linear.linear_regression()
model.predict(
    data=dataset,
    data_type='xlsx',
    input_col=['Scores'],
    value=[500],
    output_col='Hour Study'
)

OUTPUT: [[62.]]
```

## Example (Classification)
```python
from easy_predictor import classification

dataset = "C:\\users\\USER\\Documents\\Dataset_file\\sentiment_tf.xlsx"
model = classification.classification()
model.predict(dataset,
              data_type='xlsx',
              input_col=['Text'],
              value=['I hate it!'],
              output_col='Sentiment')

OUTPUT: ['NEGATIVE']
```
# Multiple Inputs (Classification)
```python
model = classification.classification()
model.predict(dataset,
                      'xlsx',
                       input_col=['Text'],
                       value=['Good stuff','Very Bad','Awesome'],
                       output_col='Sentiment')
                       
OUTPUT: ['POSITIVE','NEGATIVE','POSITIVE']
```
# Multiple Inputs (Linear Regression)
```python
model = linear.linear_regression()
model.predict(dataset,
              'xlsx',
              input_col=['Study Hour'],
              value=[12.2,5,9],
              output_col='Scores')
              
OUTPUT: [103,55,80]
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

# Statistical Calculation 

## Available Statistical Function

- Mean
- Median
- Mode

**Mean**

```python
from easy_predictor import stats

dataset = "path_to_excel"
stats.mean(dataset,dtype: str,column=['Column1']) 
```

**Median**

```python
from easy_predictor import stats

dataset = "path_to_excel"
stats.median(dataset,dtype: str,column=['Column1']) 
```

**Mode**

```python
from easy_predictor import stats

dataset = "path_to_excel"
stats.mode(dataset,dtype: str,column=['Column1']) 
```

**Half**

```python
from easy_predictor import stats

dataset = "path_to_excel"
stats.half(dataset,dtype: str,column=['Column1']) # Find half values of each rows from Column1
```


## Latest Update (0.6.6)

- **User now can assign a variable to predicted value**
- **Bug Fixed**

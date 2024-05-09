# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 ```python
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()
import seaborn as sns
import matplotlib.pyplot as plt
```
## 1. LinePlot
   ```python
   x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/varshxnx/EXNO-6-DS/assets/122253525/51650fa8-d4f8-46b9-af1c-5108d80c27af)

## 2. Multiline Plot
```python
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![image](https://github.com/varshxnx/EXNO-6-DS/assets/122253525/5b96252f-e94c-4859-a220-9f3654872f85)

## Too visualize Relationships
## 1. Barchart
```python
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/varshxnx/EXNO-6-DS/assets/122253525/6f923f2c-f9be-421a-8301-70eaa4fbb86a)


## 2. Scatter Plot
```python
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/varshxnx/EXNO-6-DS/assets/122253525/3e2eadc6-8bbe-42cd-bbc7-784c2cb705e8)


## 3.Bubble Chart
```python
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![image](https://github.com/varshxnx/EXNO-6-DS/assets/122253525/379c09d0-a971-49c4-a2bf-9615ef5b171a)

## To capture distributions
## 1.Histogram
```python
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/varshxnx/EXNO-6-DS/assets/122253525/08b8857b-caeb-477f-8829-2689544a0b5b)

## 2.Box Plot
```python
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/varshxnx/EXNO-6-DS/assets/122253525/9156f13d-f1a8-469c-93f5-4920eb1bf382)

## 3. Violin plot
```python
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/varshxnx/EXNO-6-DS/assets/122253525/9b8cc51d-d63b-433a-83eb-1f34326baa3f)

## 4. Density plot
```python
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/varshxnx/EXNO-6-DS/assets/122253525/98ee1aa0-6f30-4984-80fe-6cdc1eccb936)


## 5. Heat map
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()

![image](https://github.com/varshxnx/EXNO-6-DS/assets/122253525/873b5f17-adf3-4707-8cc8-43b40eed2e47)

# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.

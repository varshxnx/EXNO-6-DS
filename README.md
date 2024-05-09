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
![image](https://github.com/KothaiKumar/EXNO-6-DS/assets/121215739/5ab7313d-9879-4482-8dd9-d52e6d7b1dd1)
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
![image](https://github.com/KothaiKumar/EXNO-6-DS/assets/121215739/b248127c-62d5-4a55-ba1d-f47eadd058b0)
## Too visualize Relationships
## 1. Barchart
```python
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/KothaiKumar/EXNO-6-DS/assets/121215739/0dba8088-8351-4420-a313-5fc2c314ced2)

## 2. Scatter Plot
```python
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/KothaiKumar/EXNO-6-DS/assets/121215739/7221e143-bbee-4303-94c0-0ec809e350eb)

## 3.Bubble Chart
```python
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![image](https://github.com/KothaiKumar/EXNO-6-DS/assets/121215739/3e33c182-25ee-4c47-9c17-70c3dda5d2b0)

## To capture distributions
## 1.Histogram
```python
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/KothaiKumar/EXNO-6-DS/assets/121215739/4793ae99-01fb-4f26-940f-ac85609a2d46)
## 2.Box Plot
```python
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/KothaiKumar/EXNO-6-DS/assets/121215739/e4cbabce-5fba-4ac0-b83f-9104d88c2b68)
## 3. Violin plot
```python
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/KothaiKumar/EXNO-6-DS/assets/121215739/ca381f0c-6cd6-40a2-867c-d23857ee0a00)

## 4. Density plot
```python
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/KothaiKumar/EXNO-6-DS/assets/121215739/353d8570-8646-4ff4-9f21-07f8ea4014dd)

## 5. Heat map
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
![image](https://github.com/KothaiKumar/EXNO-6-DS/assets/121215739/d1b1b875-6618-4d34-be87-008253aa08b8)

# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.

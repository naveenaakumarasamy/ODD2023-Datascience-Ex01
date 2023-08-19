# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE1:
```
NAME:Naveenaa A.K
reg no: 212222230094
import pandas as pd
df = pd.read_csv("/content/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name'] = df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on'] = df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network'] = df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating'] = df['rating'].fillna(df['rating'].mean())
df['current_overall_rank'] =
df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers'] = df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
```
# OUTPUT CODE1:
!(output)![Screenshot 2023-08-19 093009](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/6e4b9106-d204-4291-8b3c-42f9e3902a66)
![Screenshot 2023-08-19 093120](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/35b8338a-eab4-4249-ba40-3a8971433ed6)
![Screenshot 2023-08-19 093046](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/9dfc5944-fd9a-42e0-a586-75dab4b0b284)
![Screenshot 2023-08-19 093145](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/4dcf611d-b988-40d4-b60c-9a0efec70e16)
![Screenshot 2023-08-19 093158](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/26ee9155-bae8-471b-9b54-11ee02394052)
![Screenshot 2023-08-19 093216](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/fb06580a-6ea1-417b-b741-8957611a44eb)
# code2:
```
NAME: Naveenaa A.K
reg no : 212222230094
import pandas as pd
import numpy as np
import seaborn as sns
df = pd.read_csv("/content/Loan_data.csv")
df
df.head()
df.describe()
df.tail()
df.isnull()
df.isnull().sum()
df.shape
df.columns
df.duplicated
#Using mode method to fill the data in columns as Object(String)
#mode()[0] - Takes the most reccuring value and fills the empty cells
df['Gender'] = df['Gender'].fillna(df['Gender'].mode()[0])
df['Dependents'] = df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Self_Employed'] = df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
#Using mean method to fill the data
df['LoanAmount'] = df['LoanAmount'].fillna(df['LoanAmount'].mean())
df['Loan_Amount_Term'] = df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['Credit_History'] = df['Credit_History'].fillna(df['Credit_History'].mean())
sns.boxplot(y="LoanAmount",data=df)
#Checking the total no.of null values
again
df.isnull().sum()
#Checking info of the dataset to check all the columns have entries
df.info()
```
# OUTPUT code2:
![Screenshot 2023-08-19 093756](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/84c4cbca-4c63-47d3-9145-e907288ac0ed)
![Screenshot 2023-08-19 093820](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/5a1c114a-b713-43d5-b3a0-d386d0ec5385)
![Screenshot 2023-08-19 093836](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/0fd00070-e67f-49fe-a65f-65d15a4c06ab)
![Screenshot 2023-08-19 093850](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/0d736034-e12b-4849-80bb-4d293e8aea24)
![Screenshot 2023-08-19 093910](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/16101005-7ffe-49cf-8f57-28591fbbab22)
![Screenshot 2023-08-19 093930](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/7ab2417c-439e-498c-acb7-eccb4ff4b631)
![Screenshot 2023-08-19 093943](https://github.com/naveenaakumarasamy/ODD2023-Datascience-Ex01/assets/113497406/f63b4b83-95de-41a2-9022-2dfd4432ecd2)
# Result:
Thus the given data is read,cleansed and cleaned data is saved into the file.


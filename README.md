# Ex03-Univariate-Analysis
## Aim:
To read the given data and perform the univariate analysis with different types of plots.

## Explanation:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

## Algorithm:
## Step1
Read the given data.

## Step2
Get the information about the data.

## Step3
Remove the null values from the data.

## Step4
Mention the datatypes from the data.

## Step5
Count the values from the data.
#  Program:
```
Developed By : ABINAYA S
Register number: 212222230002
```
## Superstore.csv
```
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv('SuperStore.csv')
print(df)
df.head()
df.info()
df.dtypes
df['Postal Code'].value_counts()
sns.boxplot(x='Postal Code', data=df)
sns.countplot(x='Postal Code',data=df)
sns.distplot(df["Postal Code"])
df.describe()
```

## Diabetes.csv
```
import pandas as pd
import numpy as np
import seaborn as sns
df = pd.read_csv("/diabetes.csv")
df
df.info()
df.isnull().sum()
df.dtypes
df.describe()
df['Glucose'].value_counts()
sns.boxplot(x="Glucose",data=df)
sns.countplot(x="Glucose",data=df)
sns.distplot(df['Glucose'])
sns.histplot(x="Glucose",data=df)
df.skew()
df.kurtosis()
```
## employeesal.csv
```
import pandas as pd
df=pd.read_csv("/content/employeesal.csv")
df
df.info()
df.dtypes
df['Salary'].value_counts()
df.describe()
import seaborn as sns
sns.boxplot(x='Experience_Years',data=df)
sns.countplot(x="Experience_Years",data=df)
sns.distplot(df['Experience_Years'])
sns.histplot(x="Experience_Years",data=df)
df.skew()
sns.histplot(x='Salary',data=df)
sns.distplot(df['ID'])
df.kurtosis()
sns.boxplot(x='Salary',data=df)
sns.boxplot(x='Experience_Years',data=df)
```
# Output:
## Superstore.csv
![O1 1](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/38a3ac73-041c-404e-93c6-c180fa91f1d9)
![O](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/680e4fe4-e029-4dc4-9a08-4c8573af505e)
![O2](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/0d8ef78b-820b-4783-8e34-4bcd8c45203b)
![O3](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/4aaa14c8-d7e6-42de-b057-5aa40fdfeaa3)
![O4](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/19f878af-4a76-45a6-9aa6-6749832725c0)
![O5](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/87fe1231-0142-4465-a675-bd57bcf82dfa)
![O6](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/da570c24-3faa-4abc-adb3-56ee3ae4c935)
![O7](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/7935dcba-a8d1-4eb6-86ed-2c39946a3e71)
![O8](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/a3f30164-4e9d-4b64-a7b4-1cd19dc93c69)
![O9](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/0b19401c-bb57-49d7-8c33-a020a1a67c63)

## Diabetes.csv
![D1](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/46f198fd-022d-4bc7-b5ec-3be4b7020fd4)
![D2](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/279557d1-0eb8-419e-b58d-42fbc8b74205)
![D3](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/2fe12adf-cfee-4451-8eb1-fa964db26bee)
![D4](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/6f5f2654-89da-413b-b198-65770fe00d74)
![D5](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/409a6144-9c12-451a-8e53-9078650f3a0d)
![D6](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/ce46fb8d-d783-448c-883b-daa6f774e1de)
![D7](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/0d138519-ff86-4b7c-8052-7647125f26cd)
![D8](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/09272c78-409e-47a2-9c9e-2352f02b5916)
![D9](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/f222d56a-65cb-4185-b74a-9e094738b967)
![D10](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/5b9a8570-9bdd-4823-ac04-fb69f11d5e26)
![D11](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/2aea7c58-682f-4b2d-86ce-9a298de7a83d)
## employeesal.csv
![1d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/fab0095c-6bf5-4ff5-9d88-131036be16d3)
![1 1d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/ef6089a7-e47c-49cf-b19a-99e9586c10b4)
![2d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/9b90eb97-dc80-413b-af91-2a66f503f406)
![3d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/4c275d1b-a8cf-46b0-b6b9-cba0767b78b1)
![4d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/9b29f48c-ea55-4b38-9883-163477bb2136)
![5d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/8bc8a42a-06f3-477b-a230-4d65b54bb340)
![6d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/7d9d6889-c78f-4252-b1cf-4e20ae57005b)
![7d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/338d08d7-9474-4a81-885c-875915a1a659)
![8d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/6d71b16c-3fe4-494f-a043-5d17141ac098)
![9d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/a0e539a4-cca0-4c74-b7af-365a8a4005cb)
![10d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/f2efd88f-7fc3-422b-a0c2-1ab7fd33cf24)
![11d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/ca4c68af-5091-46b4-b015-9f491e6ec0fd)
![12d](https://github.com/abinayasangeetha/ODD2023-DataScience-Ex-03/assets/119393675/45d610c5-19e3-44d4-be20-e571325d7042)



# RESULT:
Hence the univariate analysis is verified.

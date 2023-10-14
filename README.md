ODD2023-DataScience-Ex-03
Ex-03 Univariate Analysis
Aim:
To read the given data and perform the univariate analysis with different types of plots.

Explanation:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

Algorithm:
Step1:
Read the given data.

Step2:
Get the information about the data.

Step3:
Remove the null values from the data.

Step4:
Mention the datatypes from the data.

Step5:
Count the values from the data.

Step6:
Do plots like boxplots,countplot,distribution plot,histogram plot.

Program:
DEVELOPED BY : HARSHINI M

REGISTER NO : 212220220016

- Diabetes.csv
```Python 
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
df=pd.read_csv('diabetes.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
sns.boxplot(x="Glucose",data=df)
Glucose_q1 = df['Glucose'].quantile(0.25)
Glucose_q3 = df['Glucose'].quantile(0.75)
Glucose_IQR = Glucose_q3 - Glucose_q1
Glucose_low = Glucose_q1 - 1.5 * Glucose_IQR
Glucose_high = Glucose_q3 + 1.5 * Glucose_IQR
df=df[((df['Glucose']>=Glucose_low)&(df['Glucose']<=Glucose_high))]
sns.countplot(x="Glucose",data=df)
sns.distplot(df['Glucose'])
sns.histplot(x="Glucose",data=df)
Output(diabetes.csv) :
1 2 3 4 5 6 7 8
SuperStore.csv:
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
df=pd.read_csv('SuperStore.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
df['Postal Code']=df['Postal Code'].fillna(method='ffill')
sns.boxplot(x='Postal Code', data=df)
sns.countplot(x='Postal Code',data=df)
sns.distplot(df["Postal Code"])
sns.histplot(x="Postal Code",data=df)
Output(SuperStore.csv) : 1 1 1 2 1 3' 1 4 1 5 1 6 1 7 1 8
employeesal.csv:
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
df=pd.read_csv('employeesal.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
sns.boxplot(x='Experience_Years',data=df)
sns.countplot(x="Experience_Years",data=df)
sns.distplot(df['Experience_Years'])
sns.histplot(x="Experience_Years",data=df)
Output(employeesal.csv) : 2 1 2 2 2 3 2 4 2 5 2 6 2 7 2 8
Result:
Thus we have read the given data and performed the univariate analysis with different types of plots.

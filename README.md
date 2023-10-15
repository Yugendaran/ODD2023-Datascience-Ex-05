# Ex:05 Feature Generation
## AIM:
To read the given data and perform Feature Generation process and save the data to a file.

## Explanation:
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

## ALGORITHM:
STEP 1:Read the given Data.

STEP 2:Clean the Data Set using Data Cleaning Process.

STEP 3:Apply Feature Generation techniques to all the feature of the data set.

STEP 4:Save the data to the file.

## Program:
Developed by: YUGENDARAN G

Register number: 212221220063

## For Encoding.csv file:
```
import pandas as pd
df=pd.read_csv('Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```
## Data.csv:
```
import pandas as pd
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```
## BMI.csv file:
```
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2
```

## OUTPUT:

## For Encoding.csv

## Initial value:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/8a464bd9-0bcc-4aa6-9191-076ab36629c1)
```
## Unique value:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/356df4ef-b067-4333-816c-73c0c8fa7261)
```
## Ordinal encoder:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/a6439af4-c6d3-4023-89d1-a13768f89b7f)
```
## Label encoder:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/f9a0bbcd-14e7-4462-a123-1bd49ffa7c49)
```
## Binary encoder:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/499bcb92-009d-4407-aed5-b278c4b98c6b)
````

## For Data.csv file:
## Initial data:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/beaddcda-a10d-4bd8-a633-c1cb51f90e7b)
```
## Unique data:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/9daa9b18-fbe3-4690-a9d2-d4718b3f62db)
```
## Ordinal encoder:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/68b46e3d-5b13-4996-8264-82f3cc72d73c)
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/aaf7d585-8b08-47dc-a9af-9f376e469884)
```
## Label encoder:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/2429f88c-52bb-44a1-a0d1-a96a91d19dce)
```
## Binary encoder:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/8d4e955c-707e-45df-b746-ddfdfff436c5)
```
## For BMI.csv file:
## Initial data:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/91c59733-90f8-4f2a-96d7-34eb0f5f40bb)
```
## Binary encoders:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/2d5b8185-2d0b-46fc-923e-223c9f93bdf8)
```
## Dummies:
```
![image](https://github.com/Yugendaran/ODD2023-Datascience-Ex-05/assets/128135616/2243de98-0f19-4657-9ed4-3e19fda8530d)
```
## RESULT:
The Feature Generation process was performed and saved the data to a file.

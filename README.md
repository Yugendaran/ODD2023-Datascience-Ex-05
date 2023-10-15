# Ex:05 Feature Generation
##AIM:
To read the given data and perform Feature Generation process and save the data to a file.

##Explanation:
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

##ALGORITHM:
STEP 1:Read the given Data
STEP 2:Clean the Data Set using Data Cleaning Process
STEP 3:Apply Feature Generation techniques to all the feature of the data set
STEP 4:Save the data to the file

##Program:
Developed by: YUGENDARAN G
Register number: 212221220063

##For Encoding.csv file:
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
##Data.csv:
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
##BMI.csv file:
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2


##OUTPUT:

##For Encoding.csv
Initial value
273361428-f5cec2f4-94be-40fa-b2c3-a59adfa35529

Unique value:
273361494-029ec726-bdca-45f7-a02e-ad869bd56ee4

Ordinal encoder:
273361536-cbc90934-c85e-4e60-b062-aa17f7848e1c

Label encoder:
273361563-be7e341c-e66a-4522-9daa-ca58e835d491

Binary encoder:
273361584-6a474ae4-4f11-445a-97b7-a138b89096da 273361597-7d9da7e9-83e6-4331-a573-30e11e6e3f7b

For Data.csv file:
Initial data:
273361639-97e763d2-5d13-4557-ac74-013d5dbafc31

Unique data:
273361675-b6eeb54b-fa73-453c-8633-e6d2683e188e

Ordinal encoder:
273361705-0347af5e-9372-4e3d-8d6c-37624bf491ad 273361778-b40cb7fe-2307-49fe-b5b4-c8fc0cc6a92e

Label encoder:
273361807-1fa70e48-0138-4374-a692-f1bbb8f31296

Binary encoder:
273361833-b1289098-ce15-417b-9fda-aa597b70ea47 273361842-4d218dd6-737b-461b-af77-e7f84210dd55

For BMI.csv file:
Initial data:
273361857-27089f7d-ef4b-47f9-b281-55f1851c535d

Binary encoders:
273361897-f5908604-451a-4c35-89fb-03d480ee3126

Dummies:
273361998-aaf349a3-ae1d-4273-9652-ef413ff37f3d

##RESULT:
The Feature Generation process was performed and saved the data to a file.

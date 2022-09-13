# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```py
import pandas as pd
import numpy as np
import seaborn as sns
df = pd.read_csv("Data_set.csv")
df
df.head()
df.describe()
df.info()
df.tail()
df.shape
df.columns
df.isnull().sum()
df.duplicated()
df['show_name']= df['show_name'].fillna(df['show_name'].mode()[0])
df['aired_on']= df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']= df['original_network'].fillna(df['original_network'].mode()[0])
sns.boxplot(x="rating",data=df)
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df['watchers']=df['watchers'].fillna(df['watchers'].mean())
df.isnull().sum()
df.info()
```
# OUPUT
### Dataset:
![ds1](https://user-images.githubusercontent.com/93427254/189977182-f0a05305-4ed3-43bf-aed6-893194ea0aef.png)

### Head:
![ds2](https://user-images.githubusercontent.com/93427254/189977238-5458362e-109b-45b8-99f6-487b98ba3722.png)

### Describe:
![ds3](https://user-images.githubusercontent.com/93427254/189977232-5139f6ad-663d-4b95-831b-b95ad888c5be.png)

### Info:
![ds4](https://user-images.githubusercontent.com/93427254/189977228-40d02e24-22a7-4fa5-96e4-c26077bbb5d2.png)

### Tail:
![ds5](https://user-images.githubusercontent.com/93427254/189977225-6276307e-bacd-470e-9fb1-c50b974611e8.png)

### Shape:
![ds6](https://user-images.githubusercontent.com/93427254/189977222-545bb6b9-9dc9-4c2c-9fbd-f52f45579540.png)

### Isnull().sum()-Pre cleaning:
![ds7](https://user-images.githubusercontent.com/93427254/189977215-66ad1501-55ac-4cc5-a7e0-3f06ed1a0415.png)

### Duplicates:
![ds8](https://user-images.githubusercontent.com/93427254/189977211-4b5e629a-27ef-4605-930f-88eb6ff6f35f.png)

### SNS Plot Rating:
![ds9](https://user-images.githubusercontent.com/93427254/189977206-0910c310-3878-4476-ac77-6356f72fb93c.png)

### isnull().sum()-Post cleaning:
![ds10](https://user-images.githubusercontent.com/93427254/189977201-cc8cdd99-88a4-4e9e-a647-f197fab4bc70.png)

### Info - Post cleaning:
![ds11](https://user-images.githubusercontent.com/93427254/189977196-c8bf1c8d-6f86-4371-b713-1d8c297f60fa.png)

# RESULT:
The given data is read and data cleaning is performed and the cleaned data is saved to a file.

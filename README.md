# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output

import pandas as pd 

data=pd.read_csv("Data_set.csv")

print(data)

<img><img width="804" height="692" alt="image" src="https://github.com/user-attachments/assets/1f620b08-3054-45af-a9c3-3b607e5c5b34" />

print(data.dropna(axis=1))

<img><img width="563" height="247" alt="image" src="https://github.com/user-attachments/assets/24e588d7-f2c7-4d72-ae26-345fd546cb51" />

print(data.dropna(axis=0))

<img><img width="661" height="243" alt="image" src="https://github.com/user-attachments/assets/204d549d-11f9-4725-bd35-6b20d816d6b0" />

import pandas as pd

data=pd.read_csv("Data_set.csv")

df=pd.DataFrame(data)

print(df.fillna(method='ffill'))

<img><img width="941" height="684" alt="image" src="https://github.com/user-attachments/assets/42d6dd11-33c9-4577-97bc-3013e3408f28" />

import pandas as pd

data=pd.read_csv("Data_set.csv")

df=pd.DataFrame(data)

print(df.fillna(method='bfill'))

<img><img width="942" height="695" alt="image" src="https://github.com/user-attachments/assets/9c2a6edc-31b4-44ef-ae0d-1ac6531db756" />

import pandas as pd
data=pd.read_csv("Data_set.csv")
df=pd.DataFrame(data)
print(df.interpolate())

<img><img width="899" height="689" alt="image" src="https://github.com/user-attachments/assets/ff6697bc-6344-4214-b712-17cefeaead58" />

import pandas as pd

data=pd.read_csv("Data_set.csv")

df=pd.DataFrame(data)

print(df.mean(numeric_only=True))

<img><img width="384" height="110" alt="image" src="https://github.com/user-attachments/assets/f34d568c-bd3a-47db-8e3d-b93a0246926b" />

import pandas as pd

data=pd.read_csv("Data_set.csv")

df=pd.DataFrame(data)

print(df.median(numeric_only=True))

<img><img width="399" height="114" alt="image" src="https://github.com/user-attachments/assets/67a206e7-bf27-446f-a791-2dd0172da941" />

import pandas as pd

data=pd.read_csv("Data_set.csv")

df=pd.DataFrame(data)

print(df.mode(numeric_only=True))

<img><img width="663" height="468" alt="image" src="https://github.com/user-attachments/assets/3a803dbb-9569-4bf7-8de2-f2bb1e3b75d1" />


plt.bar(data["country"],df["num_episodes"])

plt.show()


<img><img width="650" height="393" alt="image" src="https://github.com/user-attachments/assets/4225ac61-5066-4e9f-98a7-038f356ca49d" />

plt.barh(data["country"],df["num_episodes"])

plt.show()


<img><img width="652" height="394" alt="image" src="https://github.com/user-attachments/assets/5e638041-561f-4263-a0bf-739e51a8777d" />

plt.plot(data["country"],df["num_episodes"])

plt.show()


<img><img width="767" height="402" alt="image" src="https://github.com/user-attachments/assets/a9b2adc5-f683-4f44-ada6-3beba90071d8" />

plt.scatter(data["country"],df["num_episodes"])

plt.show()



<img><img width="828" height="403" alt="image" src="https://github.com/user-attachments/assets/002cad5a-8f87-4216-818b-f95cc2edc687" />











# Result:
Thus we have cleaned the data and removed the outliers by detection using IQR and Z-score method.

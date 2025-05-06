![Screenshot 2025-04-21 182419](https://github.com/user-attachments/assets/a40bf2bc-81d9-4414-8b0e-778b015f84a2)![Screenshot 2025-04-10 110134](https://github.com/user-attachments/assets/7ae28cb8-c9f3-40a6-bcc2-e58f09e5db01)![Screenshot 2025-04-10 105657](https://github.com/user-attachments/assets/d498496e-8cda-4d20-8e9b-b24b7749b114)![Screenshot 2025-03-25 140810](https://github.com/user-attachments/assets/f35b5056-2079-4999-9ddf-4e80ebb70221)![Screenshot 2025-03-25 140738](https://github.com/user-attachments/assets/0ca1f44c-652d-4681-8791-6d7028ac4409)# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

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
```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![Screenshot 2025-05-06 143745](https://github.com/user-attachments/assets/2fa2fb17-3b5d-4349-b910-97490427ee25)
```
df = sns.load_dataset("tips")
df
```
![Screenshot 2025-05-06 143755](https://github.com/user-attachments/assets/275e61f7-601a-4f79-b98e-3e1226b341a1)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![Screenshot 2025-05-06 143803](https://github.com/user-attachments/assets/4dfc891d-5300-4656-9903-e8052237d5ad)
```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![Screenshot 2025-05-06 143809](https://github.com/user-attachments/assets/5ec02d5a-fc05-4dbb-b4b1-3b2c4a60eec0)
```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![Screenshot 2025-05-06 143824](https://github.com/user-attachments/assets/95788096-ee01-4732-99a4-b8d9c7875e10)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![Screenshot 2025-05-06 143830](https://github.com/user-attachments/assets/ab17115d-f266-4442-ae34-cafdb93b0475)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![Screenshot 2025-05-06 143838](https://github.com/user-attachments/assets/fe48ac2a-90ea-49ac-b019-6602d2fc5408)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![Screenshot 2025-05-06 143845](https://github.com/user-attachments/assets/3269022c-b591-42e3-b9fb-d85442632637)
```
tit=pd.read_csv("/content/titanic_dataset.csv")
tit
```
![Screenshot 2025-05-06 143901](https://github.com/user-attachments/assets/5d268066-e2db-4ed2-a55c-a893823dcf8d)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![Screenshot 2025-05-06 143920](https://github.com/user-attachments/assets/542a5e84-7284-40b6-8518-38be5bbd6ef0)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![Screenshot 2025-05-06 143928](https://github.com/user-attachments/assets/a0aee7bd-c7b6-438a-a58d-7befb1dd5c3b)
















# Result:
 Include your result here

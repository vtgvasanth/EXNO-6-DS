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
 ```
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/6b53da20-2502-4385-aac7-98f1f3befd8a)
```
df=sns.load_dataset('tips')
df
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/fdd20d4d-83e2-4d72-826e-261da338cefb)

```
sns.lineplot(x='total_bill',y='tip',data=df,hue='sex',linestyle='solid',legend='auto')
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/ea007708-1d9e-42f9-9985-952d60f38f30)
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi-Line Plot')
plt.xlabel('X Label')
plt.ylabel('Y Lbel')
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/62278204-c402-4521-8756-a4c3cfe074db)
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title("Average Total Bill and Tip by Day")
plt.legend()
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/9a8c998c-c0e6-4a1b-ba1f-9087a80f8311)
```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/25e9d270-63d1-46a2-903f-368eee6c7415)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/b78f792c-8825-4040-bc74-2bc9aeb004e8)
```
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/8f73de4f-93b9-48ea-9ea4-b167e921c46f)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/5fe92a80-b36e-412c-bd3a-6c55605e8d9a)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/50f6b48b-4e0f-48f2-b9a0-4ebd92538bbd)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/51cfb849-da47-4dd4-9016-15526fac6649)
```
import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/31bfecc2-5e1f-42fe-978d-8c93a3031519)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/f1a7429c-32bb-42bb-ab7f-f78338f2e60b)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/b92fbcc3-35e3-4eb5-9f42-71302555e061)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/15d431e2-45f8-4aaf-bd09-a09293fe45c3)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/bd0c4516-7f6f-4e74-a8fd-9828f561479e)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/e6097c2a-2000-435b-baa6-25d5a4f871ee)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
palette="Set3", inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/0aa05fec-1331-4a9f-a6b7-1d7382d830ad)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/9625f124-7646-4a9b-ba5f-1436dd70f60a)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/274f0dd5-db9e-4627-af64-d1492e8d59e0)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/ca789b30-eb66-480b-9aae-fd3624ffe652)
```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/ac7ea457-9bb0-4892-8e4d-a0cdc9584696)
```
sns.kdeplot(data=mart)
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/8ff7b89b-420a-487c-9128-d487e6b0954b)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/51ae93b7-e5e1-4bc4-ab02-c18789adefa0)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/a33e47db-3c01-42ec-aa4c-32de42bfa024)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/f9e5c308-2b66-4e1a-aa44-2129179bd8ef)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/22008650/EXNO-6-DS/assets/122548204/180369ae-c880-4a67-98d0-4e60af889b8c)

# Result:
 Thus, all the data visualization techniques of seaborn has been implemented.

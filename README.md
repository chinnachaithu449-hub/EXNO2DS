# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
~~~
import pandas as pd  
df=pd.read_csv("titanic_dataset.csv")  
print(df)
~~~  
<img width="903" height="816" alt="image" src="https://github.com/user-attachments/assets/07c2d70d-552e-4d69-a617-da47627d8040" />

~~~
df.info()
~~~
  
<img width="405" height="365" alt="image" src="https://github.com/user-attachments/assets/d927dcf9-8383-47c0-8560-0508eb710557" />

~~~
df.dtypes
~~~
<img width="290" height="297" alt="image" src="https://github.com/user-attachments/assets/a02fa669-7efb-4987-ab2b-b16bc0386f23" />

~~~
df.shape
~~~  
<img width="186" height="30" alt="image" src="https://github.com/user-attachments/assets/fbdbb6c9-41c5-421e-bc67-5b20fa61a54b" />

~~~
 df.describe()
~~~  
 <img width="842" height="286" alt="image" src="https://github.com/user-attachments/assets/053c1fae-e4d0-47c6-a1ba-18074be1860b" />
 
~~~
df.value_counts()
~~~  
<img width="1070" height="487" alt="image" src="https://github.com/user-attachments/assets/2de9d9a5-9350-48db-aacd-f7338f8b667b" />

~~~
df["Survived"].value_counts()
~~~ 
<img width="427" height="75" alt="image" src="https://github.com/user-attachments/assets/f9c3308c-42b5-42de-8ab3-132d2266c7b6" />

~~~
df.nunique()
~~~ 
<img width="400" height="302" alt="image" src="https://github.com/user-attachments/assets/d088f19a-2fa5-4580-a68e-5a8eb9a66318" />

~~~
import seaborn as sns   
sns.boxplot(data=df,x="Age")
~~~

<img width="807" height="567" alt="image" src="https://github.com/user-attachments/assets/1bbff6f7-2f6e-4d1a-991f-b1f8b0aae45a" />

~~~
sns.countplot(data=df,x="Survived")
~~~
 
<img width="876" height="567" alt="image" src="https://github.com/user-attachments/assets/27f110a4-8ced-47a1-8888-1808e9289dfb" />

~~~
sns.histplot(data=df,x="Age")
~~~  
<img width="868" height="537" alt="image" src="https://github.com/user-attachments/assets/90137003-a600-4a83-9816-c7d3962ea18c" />

~~~
df.rename(columns={'Sex':'Gender'},inplace=True)  
df
~~~  
<img width="1085" height="505" alt="image" src="https://github.com/user-attachments/assets/ed2afa6c-255c-43c0-ba6d-787cf6f30345" />

~~~
sns.scatterplot(x=df['Age'],y=df['Fare'])
~~~ 
<img width="902" height="565" alt="image" src="https://github.com/user-attachments/assets/272dbb22-2dbc-435d-ac29-4c9cbd82fc4d" />
~~~
sns.boxplot(x=df['Age'],y=df['Fare'])
~~~
<img width="867" height="587" alt="image" src="https://github.com/user-attachments/assets/c2f8a5fd-0cec-40b7-8652-064c014ef68e" />

~~~
sns.barplot(x=df['Age'],y=df['Survived'])
~~~
<img width="861" height="607" alt="image" src="https://github.com/user-attachments/assets/fb756b45-34df-49d2-a5f0-38c5ba8e4573" />

~~~
sns.boxplot(x="Pclass",y="Age",hue="Gender",data=df)
~~~ 
<img width="853" height="577" alt="image" src="https://github.com/user-attachments/assets/9b2a4343-52a1-4d58-ae1c-86f9b9606a18" />

~~~
sns.catplot(data=df,col='Survived',x='Gender',hue='Pclass',kind='count')
~~~ 
<img width="1112" height="565" alt="image" src="https://github.com/user-attachments/assets/176f595a-960a-41d4-96a1-49babeafa588" />

~~~
sns.heatmap(df.corr())
~~~
<img width="927" height="615" alt="image" src="https://github.com/user-attachments/assets/317342a6-a93a-44c3-9452-26a2677d677f" />



# RESULT
        EDA Analysis on the given data set has successfully uploaded

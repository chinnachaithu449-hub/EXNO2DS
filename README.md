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
import pandas as pd  
df=pd.read_csv("titanic_dataset.csv")  
print(df)  
<img width="903" height="816" alt="image" src="https://github.com/user-attachments/assets/07c2d70d-552e-4d69-a617-da47627d8040" />

df.info()   
<img width="405" height="365" alt="image" src="https://github.com/user-attachments/assets/d927dcf9-8383-47c0-8560-0508eb710557" />

df.dtypes   
<img width="290" height="297" alt="image" src="https://github.com/user-attachments/assets/a02fa669-7efb-4987-ab2b-b16bc0386f23" />

df.shape   
<img width="186" height="30" alt="image" src="https://github.com/user-attachments/assets/fbdbb6c9-41c5-421e-bc67-5b20fa61a54b" />

 df.describe()   
 <img width="842" height="286" alt="image" src="https://github.com/user-attachments/assets/053c1fae-e4d0-47c6-a1ba-18074be1860b" />

df.value_counts()   
<img width="1070" height="487" alt="image" src="https://github.com/user-attachments/assets/2de9d9a5-9350-48db-aacd-f7338f8b667b" />

df["Survived"].value_counts()   
<img width="427" height="75" alt="image" src="https://github.com/user-attachments/assets/f9c3308c-42b5-42de-8ab3-132d2266c7b6" />

df.nunique()  
<img width="400" height="302" alt="image" src="https://github.com/user-attachments/assets/d088f19a-2fa5-4580-a68e-5a8eb9a66318" />

import seaborn as sns   
sns.boxplot(data=df,x="Age")      
<img width="807" height="567" alt="image" src="https://github.com/user-attachments/assets/1bbff6f7-2f6e-4d1a-991f-b1f8b0aae45a" />

sns.countplot(data=df,x="Survived")   
<img width="876" height="567" alt="image" src="https://github.com/user-attachments/assets/27f110a4-8ced-47a1-8888-1808e9289dfb" />

sns.histplot(data=df,x="Age")   

<img width="868" height="537" alt="image" src="https://github.com/user-attachments/assets/90137003-a600-4a83-9816-c7d3962ea18c" />








 









# RESULT
        <<INCLUDE YOUR RESULT HERE>>

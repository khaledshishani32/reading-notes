# pandas
---

#### Pandas is a python library used for data manipulation and statistical analysis. It is a fast and easy to use open-source library that enables several data manipulation tasks. These include merging, reshaping, wrangling, statistical analysis and much more. In this post, we will discuss how to calculate summary statistics using the Pandas library.

![](https://miro.medium.com/max/1024/0*r_8O6Lk7IWxdPatc)


---

## What pandas is capable of
- Importing and Exporting Data
- Viewing and Inspecting Data
- Selecting and Filtering Data
- Grouping and Sorting Data
- Handling Missing and Duplicate Data
- Setting and Resetting Index
- Reshaping Data
- Merging Data
- Date Formating



---

##  importing the panda's library

#### import pandas as pd
---

## Importing and Exporting Data

#### #Importing data
#### data = pd.read_csv('titanic.csv')
#### #Exporting data
#### data.to_csv('output.csv')

##### The first step in the data science project is to import the dataset. Often you will work with a common separate value(CSV) file. read_csv() function is used to import the dataset and to_csv() is used to export the dataset.

##### Data is the variable name and the variable is used to store any kind of data. Any variable name can be used. Different file formats of data can be imported and exported like Excel, Html, JSON, etc.

![](https://miro.medium.com/max/875/1*BuuyMh6TOZZFpFLjzwYgVA.png)
---


## Viewing and Inspecting Data
---
#### #Returns by default top five rows
#### data.head()
![](https://miro.medium.com/max/875/1*eUfDg-aSrdSkSY7MDeqUFg.png)
---
#### #Returns by default last five rows
#### data.tail()
![](https://miro.medium.com/max/875/1*3o-FOGExIk06PlNX6Hs9ng.png)

#### #Returns column names
#### data.columns
![](https://miro.medium.com/max/820/1*pOdUknhq_J0XTdyVXSdUAQ.png)
---

## Selecting and Filtering Data
#### #Selects one column data
#### data['Name']

![](https://miro.medium.com/max/875/1*e_fizJGzzn3eZVK6jI8VNw.png)
---
## Handling Missing Data

#### #Returns True or False 
#### data.isnull()
#### data.isna()
#### #True -> NA 
#### #False -> Not NA
![](https://miro.medium.com/max/875/1*FGVTtGFq-JNDjBGTdHDkYQ.png)
---

# Conclusion
#### The Pandas library is really an amazing tool to have in Python. You can begin to see the true capabilities that Pandas has to offer when starting to work with data in Python. Learning Pandas and how it works will improve your Python experience with Data Science by allowing you to have more control over your input data. This will not only give you more flexibility and power when exploring data, but also when working directly with it to achieve your programmatic, computational, or scientific goals. 




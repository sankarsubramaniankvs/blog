---
layout: post
title: Machine Learning-#3-Preprocessing the data
date: 2020-06-18 00:00:00 +0300
description: Preprocessing the data # Add post description (optional)
img: ML.jpg # Add image post (optional)
tags: [Education, Machine Learning] # add tag
---

After [importing the dataset]({{site.baseurl}}/Machine-Learning-2) into the program, we can start to preprocess the data. The steps to preprocess the data are as follows:

---

### 1.Splitting the data into dependent and independent variables:
---

![]({{site.baseurl}}/assets/img/sp5.png)

In our example data, the independent variables are **Country, Age and Salary** and the dependent variable would be **Purchased**

To understand this, think of it as, we are going to provide you with country, age and salary and you'll have to predict whether the person will purchase the product or not. 

To put it simply, the value which you are going to predict would be dependent, and the remaining will be independent in most case.

Now we have to split the columns **Country, Age and Salary** as dependent and **Purchased** as independent.

Let the independent variable be x and the dependent variable be y.

    #splitting the data:
    x=dataset.iloc[:,:-1].values
    y=dataset.iloc[:,3].values

**iloc** is a function of pandas which is used to split a dataset.

The second line in the above code in which we define the variale x, we have the called the iloc function from **:** meaning from first, then **,** which means all rows and **3** which means upto 3rd row(not including). Here the array index starts from 0. So Country-0, Age-1, Salary-2, Purchased-3 are the corresponding indices. 

In the last line of the code, we are including all rows but only 3rd column.

The entire code would be as follows:

![]({{site.baseurl}}/assets/img/sp6.png)

To save press **ctrl+s**

After Saving, press **F5** to run the program. 

Now click on the variable explorer in the top right pane. You can find the two new variables x and y. Double click them to see that the dataset is split accordingly.

![]({{site.baseurl}}/assets/img/sp7.png)

---

### 2.Taking care of Missing Data:

In a Dataset there can be some missing data. We can take care of missing data in many ways. If it is a numerical value, we can take mean of the column. This is one of the best ways to handle missing data. We can also remove the row with missing data, but it will mostly affect our prediction accuracy. There are certain cases where we have no option but to remove the row. But for now we'll fill the missing data with mean of the column.

To take care of missing data, there is a class called Imputer in sklearn library. 

First, let us import the library.

    from sklearn.impute import SimpleImputer
    import numpy as np
    imputer = SimpleImputer(missing_values = np.nan, strategy = 'mean')
    imputer = imputer.fit(x[:, 1:3])
    x[:, 1:3] = imputer.transform(x[:, 1:3])

The numerical columns we have are Age and Salary 

The two columns are in variable x at indexes 1 and 2.

After importing the SimpleImputer class, we have created an object imputer at line 2 with mean strategy. 

In the third line, we have fitted the object according to our data. 

Finally, we transform our independent variable x.

Now save and run the file, go to variable explorer and open the variable x.

![]({{site.baseurl}}/assets/img/sp8.png)

Now that you have learnt how to preprocess data, we will start Simple Linear Regression in the next article.

**Note:** This article and the follow ups are only for absolute beginners in machie learning. I'm going really slow so as to make sure everyone is on the same page. If you are already an intermediate or expert in machine learning, then this is not for you! 

 To receive updates, follow me on social media using links available in the page or subscribe to our mailing list.. Thank You guys!
---



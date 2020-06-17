---
layout: post
title: Machine Learning-#2-Importing the Data
date: 2020-06-17 00:00:00 +0300
description: The first step in machine learning is to import the data # Add post description (optional)
img: ML.jpg # Add image post (optional)
tags: [Education, Machine Learning] # add tag
---

Hello friends, today we will start our machine learning journey starting from Data Preprocessing in python.
Before continuing, please make sure that you have installed the required software in your system as instructed in the [previous post.]({{site.baseurl}}/Machine-Learning-1)

# What is Data Preprocessing?

A formal definition of Data preprocessing would be "***Data Preprocessing is that step in which the data gets transformed, or Encoded, to bring it to such a state that now the machine can easily parse it. In other words, the features of the data can now be easily interpreted by the algorithm***". 

The machine can understand *Data* only when the data is structured. In other words, for example, a table is better understood than a free text. So structuring data in a way that machine can interpret the best possible way is what we are gonna do in preprocessing..

The first step in Data Preprocessing is to import the Data, we'll see about importing data into our program.

### 1. Download the Data to work on:

[click here]({{site.baseurl}}/assets/Data.csv) to dowload the dataset that we will work on.
Credit: The data here for practice is obtained from *towardsdatascience.com*.

Download the above file and store it in a folder called **Preprocessing**.


### 2. Open the Spyder IDE:

![]({{site.baseurl}}/assets/img/sp1.png)

After installing Anaconda, search Spyder in the start menu and open the IDE. Opening spyder may take more time than opening normal applications. So please be patient.


### 3. Setting the working Directory:

After opening Spyder, open the Preprocessing folder which contains our Data.csv file in spyder.

To do so, click the folder icon in the top right corner, where it has a option to set the working directory.

![]({{site.baseurl}}/assets/img/sp2.png)

After setting the working directory to the folder Preprocessing, wherever it is in your computer, now create a new file called preprocess.py

![]({{site.baseurl}}/assets/img/sp3.png)

### 4. Importing the data into the program:

To import the data into our program, we are gona use the python library Pandas.

To do that we must first import the library.

    import pandas as pd

The above line will import the pandas library and we can call the library using a short keyword pd.

To import the data :

    dataset = pd.read_csv("Data.csv")

After typing the two lines, run the program in spyder.

The shortcut to run a file is **F5**.

The shortcut to run a single line of code or selected lines is **ctrl+Enter**.

Now press **F5** to run the file, then in the top right pane under where we set the working directory, you can see four options, *"Variable explorer, Help, Plots, Files"*, select the variable explorer option.

![]({{site.baseurl}}//assets/img/sp4.png)

Here we can see our dataset variable here.

Double click on the **dataset** in this pane and you can see the data as below.

![]({{site.baseurl}}/assets/img/sp5.png)

So in two lines of code we've imported the data into the program.

If you have any doubts or problems related to programming basics, feel free to reach out. I have my social media links in the site. 

We will be Processing the data in the next article. To receive updates, follow me on social media using links available in the page or subsscribe to our mailing list.. Thank You guys!

**Note:** This article and the follow ups are only for absolute beginners in machie learning. I'm going really slow so as to make sure everyone is on the same page. If you are already an intermediate or expert in machine learning, then this is not for you! 

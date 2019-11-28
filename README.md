# ProjectProgrammingforDataAnalysis GMIT 2019

## Author: Arnoud van Balkom

# Life expectancy of males in Ireland

![image](https://user-images.githubusercontent.com/47186083/69768433-6ff07a00-1178-11ea-9d8e-884eef66e203.png)

## Getting started

Follow these steps to download this repository:

- Go to my repository on Github: https://github.com/Ardvb/ProjectProgrammingforDataAnalysis2019
- Click the clone or download button.
- Save the repository to your device.
- To run the program open a command interface and navigate to the folder in which the repository was saved.

## Jupyter Notebook

I used a Jupyter notebook to display my work. The Jupyter Notebook is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text. Uses include: data cleaning and transformation, numerical simulation, statistical modeling, data visualization, machine learning, and much more. https://jupyter.org/

## Running my Jupiter Notebook

- Install Jupyterlab. This is part of the Anaconda package, that can be downloaded here: https://www.anaconda.com/distribution/
- Navigate to the folder where the repository has been downloaded on the command line.
- type: Jupyter Notebook
- From the 'home' page, click on the file called "Project2019.ipynb"
- For more information on how to use Jupyter Notebook go to the Help section in the toolbar on the top of your screen.

### This repository contains my solution to below problem statement

### Problem statement
For this project you must create a data set by simulating a real-world phenomenon of
your choosing. You may pick any phenomenon you wish – you might pick one that is
of interest to you in your personal or professional life. Then, rather than collect data
related to the phenomenon, you should model and synthesise such data using Python.
We suggest you use the numpy.random package for this purpose.
Specifically, in this project you should:
- Choose a real-world phenomenon that can be measured and for which you could
collect at least one-hundred data points across at least four different variables.
- Investigate the types of variables involved, their likely distributions, and their
relationships with each other.
- Synthesise/simulate a data set as closely matching their properties as possible.
- Detail your research and implement the simulation in a Jupyter notebook – the
data set itself can simply be displayed in an output cell within the notebook.

Note that this project is about simulation – you must synthesise a data set.

### Variables used:

- Life expectancy
- Birth weight
- Birth province
- IQ
- Height

### What exactly is in this repository

I have created a dataset containing 5 different variables, all in some way correlated to life expectancy. Or so I thought.  First I investigated the variables involved, their distributions and their relationship with each other. And I found out my variable <em> birth province </em> had no correlation to any of the other variables. Therefore I decided to take this variable out of the second part this project.

## Variables explained

### Life expectancy

This variable is central in this dataset. It is the life expectancy in years of males in Ireland. It turned out 





## Packages used

### - Numpy
Numpy is a fundamental library for scientific computing in Python. It adds support for large, multi dimensional arrays and matrices. It also includes a large collection of high level mathematical functions to operate on these arrays.

### - Seaborn
Seaborn is a Python visualization library based on matplotlib, providing a high-level interface for drawing statistical graphics. I found this library to be easy to use and used it to plot swarmplots and scatterplots.

### - Matplotlib
Matplotlib is the plotting library of Numpy. It provides an object-oriented API for embedding plots into applications. I used this library to plot histograms, amongst other things.

### - Pandas
Pandas is a library providing high-performance, and easily usable data structures and data analysis tools for Python. It is built on top of Numpy, so that means Numpy is required by Pandas. I have used it to read in the excel file containing the Iris date set, amongst other things.

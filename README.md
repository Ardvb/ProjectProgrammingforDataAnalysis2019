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

### What exactly is in this repository

The end result is a simulated dataset with 1000 values for each of the variables, correlated in a realistic way.

## Part 1: Variables explained and first version of dataset

Here I explained all 5 variables and their distributions:

- Life expectancy in years for males in Ireland
- Birth weight in grams
- Birth place by province
- IQ
- Height

I chose to use integers for all variables, as that is the common way they are used in other datasets I found.
I explain which distribution I chose and why. I base my simulated data on scientific sources I found online.
This part was fairly straightforward. Using Numpy.random and Pandas to create the first version of the dataset, simulating 1000 values of each of the 5 variables, was also easy enough. The next part was tougher.

## Part 2: Relationships between the variables

In this part I try to find the correct correlations between each of the variables. I got rid of <em> birth province </em> because I found no correlation at all with any of the variables, so it seemed superfluous to include it in this part about relationships.

I spent a few hours figuring out realistic correlations between the variables, and then a good few hours more trying to figure out how to use python code the integrate those correlations into the final dataset. I just would not work for me. I could not figure out how to include the standard deviation into the formula for the correlation. Then finally I found a website that got me on the right track. [<sup>1<sup>](https://realpython.com/python-random/)
I ended up creating a function that used my correlation matrix and the standarddeviations of the normally distributed variables and by multiplying the matrices I finally found a way to take the standarddeviations into account. Now I could create my final dataset of correlated values, which was the main goal of this project. Below is an example of 20 values from the simulated dataset.
  
![image](https://user-images.githubusercontent.com/47186083/69770794-40df0600-1182-11ea-8edd-023a5344844a.png)


## Part 3: Visualizations and data check

In the final part I use the Seaborn package to visualize the dataset and check if the correlations are correctly implemented. 
I used a pairplot for a quick overview of all correlations, and a few lmplots to have a closer look at a few interesting correlations.

![image](https://user-images.githubusercontent.com/47186083/69770659-d62dca80-1181-11ea-9775-247d862b1d76.png)

In above pairplot all correlations can be seen. They are as close as I could get to the real life correlations. The one that shocked me was the clear negative correlation between height and life expectancy!

I had planned a part 4 where I would investigate if the **nearest neighbors** method that Sklearn offers us, could be used to predict the life expectancy, using the other 3 variables. However, I found it did so very poorly and was of no real use, so I decided to get rid of this chapter.

## Packages used

### - Numpy
Numpy is a fundamental library for scientific computing in Python. It adds support for large, multi dimensional arrays and matrices. It also includes a large collection of high level mathematical functions to operate on these arrays.

### - Seaborn
Seaborn is a Python visualization library based on matplotlib, providing a high-level interface for drawing statistical graphics. I found this library to be easy to use and used it to plot swarmplots and scatterplots.

### - Matplotlib
Matplotlib is the plotting library of Numpy. It provides an object-oriented API for embedding plots into applications. I used this library to plot histograms, amongst other things.

### - Pandas
Pandas is a library providing high-performance, and easily usable data structures and data analysis tools for Python. It is built on top of Numpy, so that means Numpy is required by Pandas. I have used it to read in the excel file containing the Iris date set, amongst other things.

## References

1. https://realpython.com/python-random/

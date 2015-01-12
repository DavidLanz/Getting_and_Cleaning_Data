# Getting_and_Cleaning_Data

### Overview
This is a repository for any and all code written for the Getting and Cleaning Data Coursera course through Johns Hopkins University.


## Course Project

Here are the data for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
Unzip the source (https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) into a folder on your local drive, say C:\Users\%yourname%\Documents\R\

Put run_analysis.R into C:\Users\%yourname%\Documents\R\UCI HAR Dataset\

In RStudio:
setwd("C:\\Users\\%yourname%\\Documents\\R\\UCI HAR Dataset\\")
source("run_analysis.R")

then it will generate a new file TidyData.txt in your working directory.

### Evaluation Checklist

### Data Analysis Explanation

#### For 1st tiny data set:

- Read data sets and combine them
- Read subjects and combine them
- Read data labels and combine them
- Read features list
- Subset only only std and mean features from list
- Perform same subset on data set
- Rename features to be more human readable
- Read activity list
- Rename activities to be more human readable
- Rename data labels with activity name
- Merge data, subjects, and labels to single tiny data set
- Write tiny data set to file

#### For 2nd tiny data set: average of measurement for activity and subject

- Prepare empty data set of appropriate length for 
- Loop through subjects, then subloop through activities
- For each activity in a subject, get the full list of measurements
- Calculate the mean of each of these activities
- Place the means in subsequent columns of the subject/activity row
- Write second tiny data set to file

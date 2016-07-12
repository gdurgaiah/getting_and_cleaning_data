Getting and Cleaning Data: Course Project
Introduction

Goal: 
The goal of this project is to obtain the data, and prepare the tidy data by cleaning the data

Data:
The data for the project is obtained from the following URL:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip


Teh project includes a R script called run_analysis.R that does the following:

1. Merges the training and the test sets to create one data set. It reads all the test and training files: y_test.txt, subject_test.txt and X_test.txt.
It combine the files to a data frame in the form of subjects, labels, the rest of the data.We can use combine the respective data in training and test data sets corresponding to subject, activity and features. The results are stored in subject, activity and features.

2. Extracts only the measurements on the mean and standard deviation for each measurement.Read the features from features.txt and filter it to only leave features that are either means or standard deviations . A new data frame is then created that includes subjects, labels and the described features.

3. Uses descriptive activity names to name the activities in the data set. Reads the activity labels from activity_labels.txt and replace the numbers with the text.

4. Labels the data appropriately with descriptive activity names.

5. Creates a tidy data set with the average of each variable for each activity and each subject. Writes the new tidy set into a text file called tidy_data.txt, formatted similarly to the original files.

Installed Packages:
Requires the plyr, dplyr & reshape2 packages.


About the raw data

The UCI HAR Dataset must be extracted and available in a directory called "UCI HAR Dataset"

The script will create a tidy data set containing the means of all the columns per test subject and per activity. This tidy dataset will be written to a tab-delimited file called tidy_data.txt, which can also be found in this repository.
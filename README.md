GettingAndCleaningData
======================

Coursera Project on Getting and Cleaning Data

An R script called run_analysis.R that does the following: 
1.Merges the training and the test sets to create one data set.
2.Extracts only the measurements on the mean and standard deviation for each measurement. 
3.Uses descriptive activity names to name the activities in the data set
4.Appropriately labels the data set with descriptive variable names. 
5.Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

The overall approach for this script is:
1.Download the dataset if not present. 
2.rbind two data files for training and test sets to fulfil requirement 1
3.Take only std() and mean() features, subset the dataset, thus fulfilling requirement 2; the result is in mean_and_std  
4.Load the activity labels, and replace indices with names. This completes requirement 3.
5.Combines the labels and the data set using cbind; doing that for both  mean_and_std and X. This completes requirement 4.
6.Using X, calculating an aggregate using mean for averaging, averaging over activity and subject; then save the result to a file thus completing requirement 5.

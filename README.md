GettingandCleaningDataCourseProject
===================================

Getting and Cleaning Data Course Project

run_analysis.R

The cleanup script (run_analysis.R) does the following:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names.
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

Running the script

To run the script, source run_analysis.R. You will then see the output as follows:

[run_analysis.R] Getting and Cleaning Data Project 
[run_analysis.R] Author: William Bowers 
[run_analysis.R] --- 
[run_analysis.R] Starting up. 
[run_analysis.R] Preparing to run analysis. 
[run_analysis.R] Reading datasets. 
[run_analysis.R] Getting dataset: /repos/Getting-and-Cleaning-Data-Project/data/test 
[run_analysis.R]   reading features... 
[run_analysis.R]   reading activities... 
[run_analysis.R]   reading subjects... 
[run_analysis.R] Getting dataset: /repos/Getting-and-Cleaning-Data-Project/data/train 
[run_analysis.R]   reading features... 
[run_analysis.R]   reading activities... 
[run_analysis.R]   reading subjects... 
[run_analysis.R] Joining datasets. 
[run_analysis.R] Melting. 
[run_analysis.R] Dcasting. 
[run_analysis.R] Saving clean data to: /repos/Getting-and-Cleaning-Data-Project/data/cleaned.txt 
Process

For both the test and train datasets, produce an initial dataset:
1. Extract the mean and standard deviation features (listed in CodeBook.md, section 'Extracted Features'). This is the values table.
2. Get the list of activities.
3. Put the activity labels (not numbers) into the values table.
4. Get the list of subjects.
5. Put the subject IDs into the values table.
6. Join the test and train interim datasets.
7. Put each variable on its own row.
8. Rejoin the entire table, keying on subject/acitivity pairs, applying the mean function to each vector of values in each subject/activity pair. This is the clean dataset.
9. Write the clean dataset to disk.
10. Cleaned Data

Please find the cleaned up data under cleaned.txt.

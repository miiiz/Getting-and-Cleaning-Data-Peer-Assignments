#Getting and Cleaning Data Course Peer Assignments CodeBook
? The data can be obtained from: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip  
? Steps for the run_analysis.R to clean the data:   
 1. Read X_train.txt, y_train.txt and subject_train.txt and name as ?trainData?, ?trainLabel? and ?trainSubject? variables respectively.       
 2. Read X_test.txt, y_test.txt and subject_test.txt and name as ?testData?, ?testLabel? and ?testsubject? variables respectively.  
 3. Joint ?testData?  ?trainData? to generate data frame ?joinData? and joint ?testLabel?  ?trainLabel? to generate data frame ?joinLabel? and joint ?testSubject? ?trainSubject? to generate data frame ?joinSubject?.  
 4. Read the features.txt and store in variable ?features?. We get a subset of ?joinData? to extract the measurements on the mean and standard deviation.
 5. Clean the column names of the subset. We remove the "()" and "-" symbols in the names, as well as make the first letter of "mean" and "std" a capital letter "M" and "S" respectively.   
 6. Read the activity_labels.txt file from the "./data"" folder and store in variable ?activity?.  
 7. Clean the activity names in the second column of ?activity?. 
 8. Transform the values of ?joinLabel? according to the ?activity? data frame.  
 9. Combine the ?joinSubject?, ?joinLabel? and ?joinData? by column to get a new cleaned data frame ?cleanedData?. 
 10. Write the ?cleanedData? out to "merged.txt" file.  
 11. Finally, generate a second independent tidy data set with the average of each measurement for each activity and each subject by initializing the ?result? data frame and performing the two for-loops.
 12. Write the ?result? out to "means.txt" file. 


Human Activity Recognition Using Smartphones Dataset

Abstract: Human Activity Recognition database built from the recordings of 30 subjects performing activities of daily living (ADL) while carrying a waist-mounted smartphone with embedded inertial sensors.
Data Set Information:
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

Attribute Information:
For each record in the dataset it is provided: 
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration. 
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

Data source
Here are the data for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
A full description is available at the site where the data was obtained:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

About R script
The file entitled “run_analysis.R” contains the R codes described in 5 steps according to the instructions provided in the assignment:
1-	Downloading and unzipping the data set
2-	Merging the training and the test sets to create one data set. (The rbind function was used)
2.1  Reading files (trainings tables, testing tables, feature vector, activity labels)
2.2.	 Assigning column names
2.3.	 Merging all data in one set
3-	 Extracting only the measurements on the mean and standard deviation for each measurement (After extracting the columns, they are given the correct names taken from features.txt)
3.1 Reading column names
3.2 Create vector for defining ID, mean and standard deviation
3.3 Making necessary subset from setAllInOne
4-	 Using descriptive activity names to name the activities in the data set
5-	 Creating a second, independent tidy data set with the average of each variable for each activity and each subject
5.1 Making second tidy data set
5.2 Writing second tidy data set in txt file 

About the variables
•	x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.
•	“Features” contains the correct names of the dataset, which are applied to the column names. A numeric vector was used to extract the desired data. 
•	A similar approach is taken with activity names through the activity variable
•	setAllInOne is the merged data set from the training and the test sets.
•	secTidySet is a second independent tidy data set with the average of each variable for each activity and each subject. This variable was renamed run_analysis.R based on the instructions listed in the assignment




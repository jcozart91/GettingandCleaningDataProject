**Data Set Information:**

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

Check the README.txt file for further details about this dataset. 

A video of the experiment including an example of the 6 recorded activities with one of the participants can be seen in the following link: [Web Link]

An updated version of this dataset can be found at [Web Link]. It includes labels of postural transitions between activities and also the full raw inertial signals instead of the ones pre-processed into windows.


**Attribute Information:**

For each record in the dataset it is provided: 
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration. 
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

**Description of Content**

This is a code book that describes the variables, the data, and any transformations or work that was performed to clean up the data.

**1st Section: Merging the training and tests scores to create one data set**
1. Read in files, assign column names, and merge.
2. Files read in from:
* features.txt
* activity_labels.txt
* subject_train.txt
* x_train.txt
* y_train.txt
* subject_test.txt
* x_test.txt
* y_test.txt

**2nd Section: Extracts only the measurements on the mean and standard deviation for each measurement**

Create a logical vector that contains TRUE values for the ID, mean, and stdev columns and FALSE for others. Subset data.

**3rd Section: Use descriptive names to name the acitivties in the sata set**

Merge the finalData set with the acitivityType table to include descriptive activity names.

**4th Section: Appropriately label the data set with the decriptive acitivity names**

Use the gsub function to clean up the data labels.

**5th Section: Create a second, independent tidy data set with the average of each variable for each activity and each subject **

Produces a data set with the average of each variable for each acitivty and subject.






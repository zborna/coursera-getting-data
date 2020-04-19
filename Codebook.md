## Code Book

This code book describes the data used by *run_analysis.R*, and the definition of variables in *output/tidydata.txt*.

## Dataset Used

This data is obtained from "Human Activity Recognition Using Smartphones Data Set". The data linked are collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site <http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones>.

The data set used can be downloaded from <https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip>. 

### For each record it is provided:

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

### Explanation of each file

- `features_info.txt`: Shows information about the variables used on the feature vector.
- `features.txt`: List of all features.
- `activity_labels.txt`: Links the class labels with their activity name.
- `train/X_train.txt`: Training set.
- `train/y_train.txt`: Training labels.
- `test/X_test.txt`: Test set.
- `test/y_test.txt`: Test labels.


## Transformations

Following are the transformations that were performed on the input dataset:

-  from `X_train.txt` only columns with the measurements on the mean and standard deviation are kept.
- `X_train.txt`, `y_train.txt` and `subject_test.txt` are loaded and combined into single data.frame `train`
- `X_train.txt`, `y_train.txt` and `subject_test.txt` after merging are filled with NULL

-  from `X_test.txt` only columns with the measurements on the mean and standard deviation are kept.
- `X_test.txt`, `y_test.txt` and `subject_test.txt` are loaded and combined into single data.frame `test`
- `X_test.txt`, `y_test.txt` and `subject_test.txt` after merging are filled with NULL

- `train` and `test`are combined into final data.frame `data`
- `data` columns labels are transformed with descriptive variable names
- an independent tidy data set is created with the average of each variable for each activity and each subject.



## Output Data Set

The output data *output/tidydata.txt* is in a space-delimited value file. 


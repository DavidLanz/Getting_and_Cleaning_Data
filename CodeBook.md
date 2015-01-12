## Code Book for Course Project

### Overview

[Source](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) of the original data:

	https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

	
### Process

The script `run_analysis.R` performs the following process to clean up the data
and create tiny data sets:

1. Merge the training and test sets to create one data set.

2. Reads `features.txt` and uses only the measurements on the mean and standard
   deviation for each measurement. 

3. Reads `activity_labels.txt` and applies human readable activity names to
   name the activities in the data set.

4. Labels the data set with descriptive names. (Names are converted to lower
   case; underscores and brackets are removed.)

5. Merges the features with activity labels and subject IDs. The result is
   saved as `tidyData.txt`.

6. The average of each measurement for each activity and each subject is merged
   to a second data set. The result is saved as `TidyData.txt`.

### Variables

- x_test - table contents of `test/X_test.txt`
- x_train - table contents of `train/X_train.txt`
- x - Measurement data. Combined data set of the two above variables
- subject_test - table contents of `test/subject_test.txt`
- subject_train - table contents of `test/subject_train.txt`
- s - Subjects. Combined data set of the two above variables
- y_test - table contents of `test/y_test.txt`
- y_train - table contents of `train/y_train.txt`
- y - Data Labels. Combined data set of the two above variables. 
- features - table contents of `features.txt`
- featindex_featuresures - Names of for data columns derived from featuresList
- activities - table contents of `activity_labels.txt`. Human readable
- tidyDataSet - subsetted, human-readable data ready for output according to project description.
- tidyDataAVGSet - second tiny data set with average of each variable for each activity and
  subject

### Output

#### tidyData.txt

`tidyData.txt` is a 10299x68 data frame.

- The first column contains subject IDs.
- The second column contains activity names.
- The last 66 columns are measurements.
- Subject IDs are integers between 1 and 30.

#### TidyData.txt

`TidyData.txt` is a 180x68 data frame.

- The first column contains subject IDs.
- The second column contains activity names.
- The averages for each of the 66 attributes are in columns 3-68.

# Human-Activity-Recognition
This project is to build a model that predicts the human activities such as Walking, Walking_Upstairs, Walking_Downstairs, Sitting, Standing or Laying.
This dataset is collected from 30 persons(referred as subjects in this dataset), performing different activities with a smartphone to their waists.
The data is recorded with the help of sensors (accelerometer and Gyroscope) in that smartphone. This experiment was video recorded to label the data manually.
# How data was recorded
By using the sensors(Gyroscope and accelerometer) in a smartphone, they have captured '3-axial linear acceleration'(_tAcc-XYZ_) from accelerometer and '3-axial angular velocity' (_tGyro-XYZ_) from Gyroscope with several variations.
prefix 't' in those metrics denotes time.
suffix 'XYZ' represents 3-axial signals in X , Y, and Z directions.
# Feature names
1. These sensor signals are preprocessed by applying noise filters and then sampled in fixed-width windows(sliding windows) of 2.56 seconds each with 50% overlap. ie., each window has 128 readings.</br>
2. From Each window, a feature vector was obtianed by calculating variables from the time and frequency domain.
In our dataset, each datapoint represents a window with different readings.</br>
3. The accelertion signal was saperated into Body and Gravity acceleration signals(tBodyAcc-XYZ and tGravityAcc-XYZ) using some low pass filter with corner frequecy of 0.3Hz.</br>
4. After that, the body linear acceleration and angular velocity were derived in time to obtian jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ).</br>
5. The magnitude of these 3-dimensional signals were calculated using the Euclidian norm. This magnitudes are represented as features with names like tBodyAccMag_, _tGravityAccMag_, _tBodyAccJerkMag_, _tBodyGyroMag and tBodyGyroJerkMag.</br>
6. Finally, We've got frequency domain signals from some of the available signals by applying a FFT (Fast Fourier Transform). These signals obtained were labeled with prefix 'f' just like original signals with prefix 't'. These signals are labeled as fBodyAcc-XYZ, fBodyGyroMag etc.,.</br>
7. These are the signals that we got so far.</br>
tBodyAcc-XYZ</br>
tGravityAcc-XYZ</br>
tBodyAccJerk-XYZ</br>
tBodyGyro-XYZ</br>
tBodyGyroJerk-XYZ</br>
tBodyAccMag</br>
tGravityAccMag</br>
tBodyAccJerkMag</br>
tBodyGyroMag</br>
tBodyGyroJerkMag</br>
fBodyAcc-XYZ</br>
fBodyAccJerk-XYZ</br>
fBodyGyro-XYZ</br>
fBodyAccMag</br>
fBodyAccJerkMag</br>
fBodyGyroMag</br>
fBodyGyroJerkMag</br>
8. We can esitmate some set of variables from the above signals. ie., We will estimate the following properties on each and every signal that we recoreded so far.</br>
mean(): Mean value</br>
std(): Standard deviation</br>
mad(): Median absolute deviation</br>
max(): Largest value in array</br>
min(): Smallest value in array</br>
sma(): Signal magnitude area</br>
energy(): Energy measure. Sum of the squares divided by the number of values.</br>
iqr(): Interquartile range</br>
entropy(): Signal entropy</br>
arCoeff(): Autorregresion coefficients with Burg order equal to 4</br>
correlation(): correlation coefficient between two signals</br>
maxInds(): index of the frequency component with largest magnitude</br>
meanFreq(): Weighted average of the frequency components to obtain a mean frequency</br>
skewness(): skewness of the frequency domain signal</br>
kurtosis(): kurtosis of the frequency domain signal</br>
bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.</br>
angle(): Angle between to vectors.</br>
9. We can obtain some other vectors by taking the average of signals in a single window sample. These are used on the angle() variable' `</br>
gravityMean</br>
tBodyAccMean</br>
tBodyAccJerkMean</br>
tBodyGyroMean</br>
tBodyGyroJerkMean</br>
# Y_Labels(Encoded)
In the dataset, Y_labels are represented as numbers from 1 to 6 as their identifiers.</br>
WALKING as 1</br>
WALKING_UPSTAIRS as 2</br>
WALKING_DOWNSTAIRS as 3</br>
SITTING as 4</br>
STANDING as 5</br>
LAYING as 6</br>
# Train and test data were saperated
The readings from 70% of the volunteers were taken as trianing data and remaining 30% subjects recordings were taken for test data

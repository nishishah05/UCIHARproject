# UCIHAR project
Human Activity Recognition (HAR) refers to the capability of machines to identify various activities performed by the users. The knowledge acquired from these recognition systems is integrated into many applications where the associated device uses it to identify actions or gestures and performs predefined tasks in response.

## Dataset
We will be using a publically available dataset called UCI-HAR. The Dataset contains data for 30 participants. Each participant performed six activities while wearing a Samsung Galaxy S II smartphone on their waist (The video of the participants taking data is also available here). The smartphone's accelerometer and gyroscope captured 3-axial linear acceleration and 3-axial angular velocity. Read all the readme and info files for more information.

## Preprocessing
We will use the raw accelerometer data within the inertial_signals folder. The provided script, CombineScript.py, organizes and sorts accelerometer data, establishing separate classes for each category and compiling participant data into these classes. MakeDataset.py script is used to read through all the participant data and create a single dataset. The dataset is then split into train,test and validation set. We focus on the first 10 seconds of activity, translating to the initial 500 data samples due to a sampling rate of 50Hz.

CombineScript and MakeDataset are used to create a Dataset that will contain the train, test, and validation set. This dataset is used to train the models.

## Questions/Tasks
1. Plot the waveform for data from each activity class. Are you able to see any difference/similarities between the activities? You can plot a subplot having 6 colunms to show differences/similarities between the activities. Do you think the model will be able to classify the activities based on the data?
2. Do you think we need a machine learning model to differentiate between static activities (laying, sitting, standing) and dynamic activities(walking, walking_downstairs, walking_upstairs)? Look at the linear acceleration for each activity and justify your answer.
3. Train Decision Tree using trainset and report Accuracy and confusion matrix using testset.
4. Train Decision Tree with varying depths (2-8) using trainset and report accuracy and confusion matrix using the Test set. Does the accuracy changes when the depth is increased? Plot the accuracies and reason why such a result has been obtained.
5. Use PCA (Principal Component Analysis) on Total Acceleration to compress the acceleration timeseries into two features and plot a scatter plot to visualize different class of activities. Next, use TSFEL (a featurizer library) to create features (your choice which ones you feel are useful) and then perform PCA to obtain two features. Plot a scatter plot to visualize different class of activities. Are you able to see any difference?
6. Use the features obtained from TSFEL and train a Decision Tree. Report the accuracy and confusion matrix using test set. Does featurizing works better than using the raw data? Train Decision Tree with varying depths (2-8) and compare the accuracies obtained in Q4 with the accuracies obtained using the featured trainset. Plot the accuracies obtained in Q4 against the accuracies obtained in this question.
7. Are there any participants/ activitivies where the Model performace is bad? If Yes, Why?

# Deployment!
Utilized apps like Physics Toolbox Suite from your smartphone to collect your data in .csv/.txt format. At least 15 seconds of data is collected, trimming edges to obtain 10 seconds of relevant data. Collected 3-5 samples per activity class and reported accuracy using both featurized and raw data. You have to train on UCI dataset and test it on the data that I have collected and reported the accuracy and confusion matrix. Tested your model's performance on the collected data, explaining why it succeeded or failed.

Things to take care of:
* Ensure the phone is placed in the same position for all the activities.
* Ensure the phone is in the same alignment during the activity as changing the alignment will change the data collected and will affect the model's performance.
* Ensure to have atleast 10s of data per file for training. As the data is collected at 50Hz, you will have 500 data samples.

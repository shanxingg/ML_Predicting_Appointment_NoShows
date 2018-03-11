# **Predicting Medical Appoinment No-shows**

A person makes a doctor appointment, receives all the instructions and no-show. Who to blame?

— Why do 20% of patients miss their scheduled appointments?

In this analysis report, I performed data exploratory analysis to explore the reasons that may cause no-shows. I used different techniques to combat the imbalanced classes and also build machine learning modles to further predict this phenomena.

[Access the notebook in jupyter nbviewer](https://nbviewer.jupyter.org/github/shanxingg/ML_Medical_Appoinment_NoShows/blob/master/Medical_Appointment_NoShows.ipynb)<br>

![Doctor](https://www.questionpro.com/blog/wp-content/uploads/2015/07/preguntas_y_respuestas_2.jpg)<br><br>



## **Table of Content**

[1. Load Data Set and Python Packages](https://nbviewer.jupyter.org/github/shanxingg/ML_Medical_Appoinment_NoShows/blob/master/Medical_Appointment_NoShows.ipynb#1)
 - Load Python Packages
 - Load and Display Data Set
 
[2. Data Quality Assessment](https://nbviewer.jupyter.org/github/shanxingg/ML_Medical_Appoinment_NoShows/blob/master/Medical_Appointment_NoShows.ipynb#2)
 - Check Missing Values
 - Check Duplicated Values
 - Check Category Variables
 - Check Numerical Variables

[3. Exploratory Data Analysis and Feature Selection](https://nbviewer.jupyter.org/github/shanxingg/ML_Medical_Appoinment_NoShows/blob/master/Medical_Appointment_NoShows.ipynb#3)
 - Exploring on "ScheduledDay" and "AppointmentDay"
 - Exploring on Given Binary Dummy Variables
 - Exploring on "Neighbourhood"
 - Exploring on "Age"
 - Exploring on "Gender"
 - Exploring on "PatientId"

[4. Building Models on Imbalanced Data](https://nbviewer.jupyter.org/github/shanxingg/ML_Medical_Appoinment_NoShows/blob/master/Medical_Appointment_NoShows.ipynb#4)
 - Transforming the Data Set
 - Define Feature Matrix and Target Array
 - Prepare Data for Model Training
 - Train Model - Logistic Regression

[5. Building Models on Balanced Data](https://nbviewer.jupyter.org/github/shanxingg/ML_Medical_Appoinment_NoShows/blob/master/Medical_Appointment_NoShows.ipynb#5)
 - Create Balanced Data Set
 - Prepare Data for Model Training
 - Logistic Regression
 - Decision Tree Classifier
 - Random Forest Classifier
 - Gradient Boosting Classifier
 - Extra Trees Classifier
 - K-Nearest Neighbors Classifier

[6. Conclusion](https://nbviewer.jupyter.org/github/shanxingg/ML_Medical_Appoinment_NoShows/blob/master/Medical_Appointment_NoShows.ipynb#6)
 - Result Summary
 - Features Importance
 - Interesting Findings

[7. Limitations](https://nbviewer.jupyter.org/github/shanxingg/ML_Medical_Appoinment_NoShows/blob/master/Medical_Appointment_NoShows.ipynb#7)

[8. Future Work](https://nbviewer.jupyter.org/github/shanxingg/ML_Medical_Appoinment_NoShows/blob/master/Medical_Appointment_NoShows.ipynb#8)

[9. Reference](https://nbviewer.jupyter.org/github/shanxingg/ML_Medical_Appoinment_NoShows/blob/master/Medical_Appointment_NoShows.ipynb#9)
<br><br>



## **Visualization Excerpts**

### 1. Class Imbalance Problem

![Imbalance](https://user-images.githubusercontent.com/32560872/37251478-b6496094-24c5-11e8-9993-bceef0e0116f.png)
From the above chart we see that there are around 80% of the patients who have turned up. We see a clear class imbalance problem here. A naive approach of predicting that every one shows up gives us an accuracy of 0.8.<br>

### 2. Show-up Rate V.S. Awaiting Days

![Awaiting_days](https://user-images.githubusercontent.com/32560872/37251502-1cc5de42-24c6-11e8-8ff9-3d9f4e6f8246.png)
Although the entire distribution of Showup Rate V.S. Awaiting Days does not show a strong relationship, awaiting time for less than or equal to 10 days show a distinctly negative relationship. Especially, people who scheduled his/her appoinment on the same day will have a obviously high show-up rate and this type of situation represent 34.89% of data in entire data set.<br>

### 3. Show-up Rate V.S. Age

![Correlation_Heatmap](https://user-images.githubusercontent.com/32560872/37251518-6a03e88e-24c6-11e8-916f-ae39e356b3ac.png)
From the above Boxplot we can see that the Median Age is around 35 and the IQR is between 18 and 55. Though the BoxPlot shows few datapoints as outliers we will not consider them as true outliers for this case.
The Scatter plot of Show-up Rate V.S. Age shows an obvious piecewise relationship:
 - Age 0-14: negatively related between Age and Show-up Rate
 - Age 15-65: positively related between Age and Show-up Rate
 - Age above 65: no clear relationship<br>

### 4. Show/NoShow for Females and Males

![Prediction](https://user-images.githubusercontent.com/32560872/37251541-cce885ea-24c6-11e8-8dfa-40f750e63e59.png)
From the above visualization we can clearly see that 'Female' patients usually have more appointments that 'Male' patients. So, Gender might be an important factor. But if we closely look at the NoShow distribution across Male's and Female's it is almost the same. So, Gender may not play an important role in determining if a patient comes for a visit or not.

# **Predicting Medical Appoinment No-shows**

A person makes a doctor appointment, receives all the instructions and no-show. Who to blame?

— Why do 20% of patients miss their scheduled appointments?

110k medical appointments with its 14 variables (characteristics). Variable names are self-explanatory.

Dataset from: https://www.kaggle.com/joniarroba/noshowappointments.<br>

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

### 1. Candlestick Chart for Bitcoin
This notebook used plotly to visually show bitcoin stock price during the period from Jan. 2017 to Mar. 2018.<br>

![Candlestick](https://user-images.githubusercontent.com/32560872/37240662-81868c64-2403-11e8-8812-ddad29c2fa9e.png)


### 2. Price Fluctuation of Cryptocurrencies
This notebook used matplotlib to visually show opening, closing, highest, and lowest stock price for each of the cryptocurrency.<br>

![Price_Fluctuation](https://user-images.githubusercontent.com/32560872/37240755-811b5844-2404-11e8-8add-7acc17e7b9ce.png)


### 3. Correlation Heatmap of Cryptocurrencies
This notebook used seaborn to visually show pearson correlation coefficient to explore if BitCoin price influences price of other cryptocurrencies.<br>

![Correlation_Heatmap](https://user-images.githubusercontent.com/32560872/37240849-9fe03122-2405-11e8-8a14-2e7833285f57.png)


### 4. Prices Prediction for Bitcoin
This notebook used matplotlib to visually show 30-days price prediction for Bitcoin.<br>

![Prediction](https://user-images.githubusercontent.com/32560872/37240880-0f18a8d0-2406-11e8-92cf-e97e42fd132a.png)

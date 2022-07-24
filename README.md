# To Predict Queue Wait-Time considering a multi-stage queue in a hospital environment.

# Problem Statement Dimensions:
1. Queue under study is a multi-stage queue in a hospital environment.
2. Predict the wait time in a hospital i.e., time taken from registering a patient to the time patient walks out of the hospital.
3. Communicate the wait time to the patients in real-time. E.g., Assume a multi-stage queue in a hospital suppose from Registration of Patient, Doctor Consultation, Billing, and Medicine Counter.
4. Communicate wait-time of the patient through every queue and the approximate idea of his/her journey time.

# Design of the system
Our system consists of 4 stages in a hospital environment namely registration, consultation, billing and medication queues which are very common to any hospital environment. All the queues have their time predicted by the Artificial Neural Network Regression Model. The system is designed in such a way that it can fit into any queuing scenario after minor alterations to the system that we have prepared. The system can also adapt to a new system by preparing its own dataset (if not provided) within a few weeks and start giving accurate predictions based on previous results.

# Data Collection
We personally visited hospitals to get an idea about the time required in various queues by communicating with the registration desk’s staff members, doctors, billing staff and even the pharmacists as in how much time is required to serve an average patient. We also visited clinics of various doctors like gynaecologist, dentist, physician,etc. which are the most commonly visited doctors and got an idea about what are common diagnosis and what are their respective average diagnose times.

# Data Preparation and Training
Filtering and organizing the data collected, datasets have been prepared for different queues of the hospital and have been split into training, testing and validation datasets. We then trained our Artificial Neural Network (ANN) model on the training dataset with appropriate epochs in order to get minimum loss.

# GUI for Users
An Android Application built using Flutter framework is used for User Interaction with the solution. It consists of a simple UI that is understandable to all.
● Home Page
It consists of an Entire Journey Time Prediction button, which directs the user to the Input Form page.
● Input Form
It consists of a dropdown where the user has to select the consulting doctor and type of diagnosis and then a submit button directs the user to the Registration Queue page.
● Registration Queue Page
It consists of a Join Registration Queue button which directs the user to the page where the user can see the time until the registration process is done as well as a card is also visible at the top that indicates the predicted entire hospital journey time of the patient. Similarly, the consultation, billing and medical page has the same UI and the card bearing total time keeps on updating.

# Flowchart
![image](https://user-images.githubusercontent.com/73229846/180658059-9fd0bf6a-2011-4479-9556-aa0881d8154d.png)

# Methodology
To predict the waiting time for the clients, we must know what factors the queue is being processed such as the number of patients standing in the queue, the rate at which patients arrive in the queue, and the rate at which patients are being served. Thus, we take inputs through the users by asking them to sign up for the queue of their interest through our android app. We update this information continuously as patients keep joining or leaving the queue. All this information collected is fed to our Queue Wait-Time Predictor App which further passes this data to the Artificial Neural Network.
Since hospitals have multi-stage queues, a separate neural network is trained for different queues at different stages. These different queues have their parameters on which they are processed. Inputs are taken and training of the neural network is done according to these specific parameters.
We will take the example of a dummy patient Smith and explain one entire cycle i.e., his complete journey.
Step 1: Registration Desk
Smith signs up for the registration queue, then the system fetches the Arrival rate (per hour) along with Service rate (per hour) and gives him an approximate time that he would require one the registration queue.
There will be an option to get an approximate time for the entire journey by filling the required parameters and the system will predict the entire journey time based on the service rate.
Step 2: Consultation Desk
For the consultation time, Smith is required to provide the required parameters like the age, name, gender etc. Based on the data provided, the arrival rate and the service rate, he will be given an approximate wait time in the consultation queue by the system.
Step 3: Billing Queue
For this queue, Smith needs to sign up for the billing queue, and in a similar fashion based on the data provided, the arrival rate and service rate, he will be given an approximate wait time in the consultation queue by the system.
Step 4: Medication Desk
Similarly, for this queue, Smith needs to sign up for the medication queue, and in a similar manner based on the data provided, the arrival rate and service rate, he will be given an approximate wait time in the consultation queue by the system.
In this way, the journey of Smith comes to an end and he will be provided with the total time taken to complete the entire journey along with the comparison with predicted time.

# Hardware Specification
As the input of the parameters that affect processing of the queue is taken through the android app itself by users signing up, there is no special or dedicated hardware requirement of our project. The only hardware requirement is that the hospitals should have functioning computers to implement our system.

# Software Requirements
The Software requirements of the proposed system are given as follows:
Platform -> Android App
Coding Languages ->	Python, Dart
Framework	-> Flutter
Database	-> Cloud Firestore
External Tools	-> Scikit-learn,	NumPy,	pandas, Matplotlib, TensorFlow 2.2.0
Server	-> Firebase

# Results
1.	Authentication Page (Sign Up for the first time)

![image](https://user-images.githubusercontent.com/73229846/180658243-539b45a2-79fa-41b8-a8bf-d392f59b881d.png)

2.	Authentication Page (Log In once authenticated as a user successfully)

![image](https://user-images.githubusercontent.com/73229846/180658260-3cae0737-cf56-4599-ac8b-5bb02a178c07.png)
 
3.	Home Page

![image](https://user-images.githubusercontent.com/73229846/180658272-c4f4c0cb-177b-43ff-b650-73e0e893a004.png)

4.	Taking Input from users about their consulting doctor and type of diagnosis.

![image](https://user-images.githubusercontent.com/73229846/180658299-21d41461-8930-49a3-a479-a5094171c6cc.png)

![image](https://user-images.githubusercontent.com/73229846/180658304-d5478cb7-abe5-45e6-b7bf-00d0c39fbdc7.png)

Example: User selects Dr. Saiqa Khan (Physician)

![image](https://user-images.githubusercontent.com/73229846/180658314-4c3d2000-b238-4782-8cae-a2c9db4bf2f7.png)

User selects Chest Pain as Diagnosis

![image](https://user-images.githubusercontent.com/73229846/180658326-849925cc-3087-4063-b916-74113a74a662.png)
 
5.	Entire Journey time predicted including service times for registration, chest pain consultation, billing and pharmacy queues. Prompt to join the Registration Queue.

![image](https://user-images.githubusercontent.com/73229846/180658335-5d163ef6-2c70-49d4-b7f8-b9766b1ce379.png)
 
6.	Registration Queue wait-time predicted.

![image](https://user-images.githubusercontent.com/73229846/180658351-8bec8c18-2163-4747-963a-d89e5f42721d.png)

7.	Message to users once the timer until predicted time ends.

![image](https://user-images.githubusercontent.com/73229846/180658359-010ab7b5-ba0d-4174-8edb-ffff21fe506b.png)
 
8.	Moving towards Consultation Queue

![image](https://user-images.githubusercontent.com/73229846/180658374-c6f8468d-30fe-40c7-9611-3a2d5db94d65.png)

9.	Prompt to join the Consultation Queue.

![image](https://user-images.githubusercontent.com/73229846/180658394-a3095084-c98f-4a70-a5e1-52154d5a3b61.png)
 
10.	Consultation Time for Chest Pain Predicted

![image](https://user-images.githubusercontent.com/73229846/180658403-555e8384-8ecb-4df0-a7ea-e42df5471249.png)
 
11.	If the user quits the queue by clicking on ‘Quit Service’

![image](https://user-images.githubusercontent.com/73229846/180658415-ef789b58-7208-424e-9d6e-788ebe512de8.png)

The user is directed towards the Home Page on clicking ‘Yes’ else Dialog box is dismissed.
 
12.	Prompt to join the Consultation Billing Queue.

![image](https://user-images.githubusercontent.com/73229846/180658423-f032af9b-4d57-4540-adb8-2d4d865b1ab4.png)
 
13.	Consultation Billing Time Predicted

![image](https://user-images.githubusercontent.com/73229846/180658430-443289bb-37a1-4b9d-9d77-f719c017b566.png)
 
14.	Prompt to join the Pharmacy Queue.

![image](https://user-images.githubusercontent.com/73229846/180658437-7ee01966-bb28-4153-806c-0a51a3284be6.png)
 
15.	Pharmacy wait-time predicted.

![image](https://user-images.githubusercontent.com/73229846/180658444-9c5f07a0-2e69-4f80-a054-729b0f018b80.png)
 
16.	End Message to the user.

![image](https://user-images.githubusercontent.com/73229846/180658451-8a49be9a-315d-41c9-aace-d60be4ed8e3d.png)

# Conclusion
In this project, we have successfully provided the users an estimate of their wait-times while waiting in any of the hospital queues. In addition to this, an idea of time they would spend in the hospital completing all their tasks is provided. This helps in reducing the distress caused to clueless waiting. Queueing theory has been studied and applied on the concerned queues to study their wait-time and service-time distributions. Based on this study, the project has tried to solve a real-life problem using Deep Learning techniques.
This project contributes towards better behaviour of patients waiting in queue as it is very likely that patients would be more calm if they know when they are going to be serviced. It is an excellent instance of solving real life problems with the help of Deep Learning.

# Future Scope
In this project, prediction of wait-times is done solely on the basis of historical data collected from the hospitals. In future, we can opt for integration of hardware solutions that would collect the data every day from the hospitals at every instance required which can then be used to continuously train the neural networks at specific intervals. This will lead us to more accuracy towards prediction.
The project can further have an addition of an admin portal, which handles the administration of the queue. For instance, removal of patients from the queue after being served, admitting a new patient in the queue, displaying a message to all the users in case of any uncertain delay or any unusual circumstances at the hospital, etc can be done by the admin using the admin portal.

# Machine learning and IOT based Temperature monitoring system


This is the final capstone project done during internship in IOT BOLT

![image](https://user-images.githubusercontent.com/69953585/111018510-311f1b80-83df-11eb-86ca-b76fbe8d2b9f.png)

# Overview

Monitors the temperature of the room and sends email alert to the user if the temperature crosses the threshold limits(max and min).

Prediction of future temperature value by carrying polynomial regression.

Sends email alert to the user when there is an sudden change in the temperature by carrying z-score analysis.

# Applications of this system.
1.Monitor the temperature of the room by setting the threshold temperature values.It sends email alert to the user when the temperature exceeds the threshold temperature.
Email-“Temperature has reached  above threshold value”
Examples :cold storage, pharmacy buildings,etc

2.It carries Z-score analysis and based on input values it sets the threshold values.It  also sends email alert to the user when the temperature has dropped suddenly.
Email –“someone has opened the door”
Examples: Refrigerator door system

3. It carries polynomial regression analysis, which helps in predicting the temperature data.



# COMPONENTS    

Hardware Components , Software apps and online services

Bolt wifi module     
Bolt cloud           
LM35 sensor	       
Ubuntu server       
Piezo buzzer	      
VMware workstation       
LED	                                                                  
Mailgun             
Bread board           
Jumper wires       
Data cable


# Introduction
This project has primarily three functionalities i.e. sense the temperature of the room and send the email alert if it crosses the limit,carry out polynomial regression analysis to predict the future temperature data and carry out z-score analysis which will be able to detect the sudden change in temperature and sends the email alert to the user. Temperature monitoring systems are incredibly useful tools to monitor and manage  heat levels .The right temperature monitoring system will enable to keep track of critical temperatures at all sites. The temperature of the place can be monitored through internet using internet of things. In this project LM35 sensor is used to sense the temperature.The system will continuously monitor the temperature condition of the room and the data is stored in the cloud.In this project I used Bolt wifi module to process the data and Blot cloud to store it. And it can be monitored at anytime and anywhere from the Internet. The main purpose of this system model is to make it easy for the user to view the current temperature.I have evaluated the system and showed that the framework can be used effectively to put into practice practical Internet of things applications over existing system



# Materials
Bolt Wifi module
BOLT is an Internet of Things platform Hardware+Software that enables user to build IoT products and projects. Using BOLT, users can control and monitor devices from any part of the world.For more info visit [here](https://www.boltiot.com/)
![image](https://user-images.githubusercontent.com/69953585/111018734-96bfd780-83e0-11eb-8d8d-f9826375d960.png)

LM35- Temperature sensor
The LM35 series are precision integrated-circuit temperature sensors, whose output voltage is linearly proportional to the Celsius(Centigrade) temperature
![image](https://user-images.githubusercontent.com/69953585/111018753-b525d300-83e0-11eb-90ac-9c67d019c374.png)


Piezo Buzzer
•	A piezo buzzer is a sound producing device.
•	The main working principle is based on the theory that, whenever an electric potential is applied across a piezoelectric material, a pressure variation is generated. A piezo buzzerconsists of piezo crystals in between two conductors
![image](https://user-images.githubusercontent.com/69953585/111018767-ce2e8400-83e0-11eb-84e3-aad4cd1b6e53.png)

  LED-Light emitting diode
An LED is an electronic device that emits light when an electrical current is passed through it. ... LEDs are commonly used for indicator lights (such as power on/off lights) on electronic devices
![image](https://user-images.githubusercontent.com/69953585/111018777-e1415400-83e0-11eb-928d-6f0ddfaa6570.png)


Mailgun
Mailgun is an Email automation service. It has a very powerful set of inbuilt functions for sending emails. Developers can process their email with the help of Mailgun API
[see here](http://a5theory.com/mailgun/)
![image](https://user-images.githubusercontent.com/69953585/111018806-19489700-83e1-11eb-9d13-3fac65b75fc1.png)


VMware Workstation
VMware Workstation Pro is a hosted hypervisor that runs on x64 versions of Windows and Linux operating systems(an x86 version of earlier releases was available) it enables users to set up virtual machines (VMs) on a single physical machine, and use them simultaneously along with the actual machine
For getting some experience with different operating system .I have used this virtual os developer.You can also conduct this project in windows os itself using IDE like jupyter notebook etc

![image](https://user-images.githubusercontent.com/69953585/111018846-70e70280-83e1-11eb-84f1-1f1db4a22208.png)


Ubuntu
Ubuntu Server is a server operating system, developed by Canonical , that runs on all major architectures: x86, x86-64, ARM v7, ARM64, POWER8, and IBM System z mainframes via LinuxONE

# Methods

# Polynomial regression
Polynomial regression is a form of regression analysis in which the relationship between the independent variable x and the dependent variable y is modelled as an nth degree polynomial in x. Polynomial regression fits a nonlinear relationship between the value of x and the corresponding conditional mean of y, denoted E(y |x). Although polynomial regression fits a nonlinear model to the data, as a statistical estimation problem it is linear, in the sense that the regression function E(y | x) is linear in the unknown parameters that are estimated from the data.
Prediction Points: This number tells the Visualizer how many future data points need to be predicted. By default, the Visualizer spaces the points with the data collection time in the hardware configuration of the product. So if you set the product to collect data every 5 minutes, and select 6 prediction points, the Visualizer will predict the trend and show 6 points up to 30 minutes into the future.


 

No. Polynomial Coefficients: Polynomial Visualizer processes the given input time-dependent data, and outputs the coefficients of the function of the form:
which most closely resembles the trend in the input data. This number tells the Visualizer how many elements should be present in the function i.e. the value of n.
Frame Size: These are the number of previous data points the Visualizer will use to predict the trend of the data. For example, if you set this value to 5, the Visualizer will use the previous 5 points to predict the trend.

# Anomaly detection  by Z-score analysis

Z-score analysis is used for anomaly detection. Anomaly here means a variable's value (temperature of the surroundings) going beyond a certain range of values. The range of values is called bounds (upper bound and lower bound). These bounds are calculated using the input values, frame size and multiplication factor. The frame size is the minimum number of input values needed for Z-score analysis and the multiplication factor determines the closeness of the bounds to the input values curve.It basically works to detect any sudden change in the sensor value when someone opens the door of fridge the temperature suddenly changes and this anomaly when detected the alert message sent via Email to the user.
we calculate the Z score (Zn) for the data and use it to calculate the upper and lower threshold bounds required to check if a new data point is normal or anomalous. by formula
where Mn is taken as mean Vi is variance and Zn as Z-score.
All repeats again and again with an gap of 10 sec and continuously monitors the system 24*7
Anomaly detection is done by using Z-score analysis which utilizes this formulas to calculate the the threshold values. Based on the average of the input values it determines a threshold boundry, if there is an sudden drop in the the value beyond these range it is able to detect it and alerts messages can be sent to the user by written suitable code.

 # Circuit connections
 
 Connecting the LM35 sensor to the Bolt
 
 1.	Hold the sensor in a manner such that you can read LM35 written on it.
2.	In this position, identify the pins of the sensor as VCC, Output and Gnd from your left to right
    VCC is connected to the green wire, Output is connected to the blue wire and Gnd is connected  to the yellow wire           
3.	Using male to female  jumper wire connect the 3 pins of the LM35 to the Bolt Wifi Module as follows:
    •	VCC pin of the LM35 connects to 5v of the Bolt Wifi module.
    •	Output pin of the LM35 connects to A0 (Analog input pin) of the Bolt Wifi module.
    •	Gnd pin of the LM35 connects to the Gnd

 
 Connecting  Buzzer and LED to the bolt via bread board

Buzzer and LED  is connected to GPIO pin                                            
+ ve terminal is connected to GPIO pin 1
-ve terminal is connected to GPIO pin 4



After the circuit connections following steps are done.
Step 1: Linking the product to the bolt device
Go [here]( https://cloud.boltiot.com/) and then follow the steps below:
* Create product [here](https://docs.boltiot.com/docs/adding-a-product)
*Writing code for controling device [here](https://docs.boltiot.com/docs/using-custom-files-in-your-product)
*Link device to product [by using this link]( https://docs.boltiot.com/docs/link-device-to-a-product)

Step 2: Write a code in javascript to carry out the polynomial regression
setChartLibrary('google_chart');
setChartTitle('Pharma Monitor');
setChartType('predictionGraph'); (plots the prediction graph based on polynomial regression analysis)
setAxisName('Time','Temp');
mul(0.097); (converts the sensor input value to output temperature in degree celcius)
plotChart('time_stamp','temp');

Step 3:Sign up to the mailgun

Step 3.1: Open [this link](https://www.mailgun.com/) in browser.

Step3. 2: Click on Sign Up button

Fill all the necessary details in SIGN UP form.
Generate mailgun API key,sandbox url and senders email
 

 

Step 4: Login to the Ubuntu via virtual machine VMware

After successful login, create a file named email_conf.py  which will store all the credentials related to Mailgun.
To create a new file type sudo nano email_conf.py in the terminal. After that write below code to save all the credentials in a single file
MAILGUN_API_KEY = 'This is the private API key which you can find on your Mailgun Dashboard' 
SANDBOX_URL= 'You can find this on your Mailgun Dashboard' 
SENDER_EMAIL = 'This would be test@your SANDBOX_URL'
RECIPIENT_EMAIL = 'Enter your Email ID Here'
API_KEY = 'This is your Bolt Cloud account API key'
DEVICE_ID = 'This is the ID of your Bolt device’
FRAME_SIZE=10
MUL_FACTOR=6 

The API key and Device ID of the Bolt module can be determined as follows:
•	Connect your Bolt Device to the Bolt Cloud as per instructions given at [here](https://cloud.boltiot.com/)
•	The following screen will appear after that.The Bolt Device ID is highlighted in yellow.
 
Go to the API section to know the API Key

 
Step 5: Create an new file named buzzer.py which contains main code to collect the data from the Bolt and send Email if it crosses the threshold and carry out Z-score analysis.

Step 6: Time to run the code. To do so type sudo python3 buzzer.py in terminal

# Steps for writing the python code (buzzer.py):

STEP 1: In the code, first import the conf file which has all the credentials. Bolt python library which will fetch the data stored in Bolt cloud. The email library is also imported to send email alerts and Bolt is used for accessing data from bolt devices. The python JSON and time libraries are also imported. The math and statistics libraries will be required for calculating the Z-score and the threshold boundaries.

STEP 2: Now initialize a variable that will store the maximum and minimum threshold value. This would send an alert if temperature goes above the maximum limit and below the minimum limit

STEP 3: Z-score calculates the boundaries required for anomaly detection.This Function takes 3 input variables: hisotry_data, frame_size and factor and  checks whether enough data has been accumulated to calculate the Z-score, and if there is too much data, then the code deletes the older data.

STEP 4: Calculates the means(Mn)  and variance value of the collected data points.

STEP 5:Here we calculate the Z score (Zn) for the data and use it to calculate the upper and lower threshold bounds required to check if a new data point is normal or anomalous.

STEP 3: To fetch data from Bolt cloud, create an object called ‘mybolt’ which can access the data from Bolt. For the Bolt Cloud to identify the bolt device, provide the API key and the Device ID when creating mybolt object. To send an email, create an object of the same.

STEP 4: To continuously monitor the temperature reading, enclose the logic to fetch, compare and send the email inside an infinite loop using the ‘while True:’ statement. To exit the loop, press CTRL+C.

STEP 5: The led and buzzer system is run by the ‘digitalWrite’ function, connected to the D4 pin of Bolt.

STEP 6: The code fetches sensor value using ‘analogRead’ function which is connected to the A0 pin of Bolt.

STEP 7: The response from the Bolt cloud using the analogRead() function is in JSON format, so load the JSON data sent by cloud using Python’s JSON library.

STEP 8: The sensor value is inside a field labeled as “value” in the response. Access the JSON values using the statement ‘sensor_value = int(data[‘value’])’. This line also converts sensor reading to integer datatype.

STEP 9: This is enclosed inside a try-except block to handle any error that may occur in the code.

STEP 10: The next line of code checks if the sensor reading is with in the  limit or not. If it exceeds, then email will be sent.

STEP 11:If the above statement is true then digitalWrite() is executed on the D1 pin of the Bolt, turning ON the  led and buzzer.

STEP 12:The email to be sent containing the text “The temperature  exceed the threshold  limit” followed by sensor reading.

STEP 13:The response from mailgun will be stored inside the ‘response’ variable.

STEP 14: The status of the message is printed on the console.

STEP 15: The statement ‘time.sleep(10)’ puts the program execution on hold for 10 seconds. 

STEP 16: The next line code shows the z-score analysis to turn on the  led and buzzer using digitalWrite() function when the temperature crosses the the limit set by z-score analysis.

STEP 17: The mail sent to the user which contains the text “Someone has opened the door.”

STEP 18: The statement ‘time.sleep(10)’ puts the program execution on hold for 10 seconds


# Results

Prediction of future temperature data

2.Temperature monitoring in the room and carrying Z-score analysis ,and sending  emai alerts.








Credits-       THANKS FOR BOLT IOT





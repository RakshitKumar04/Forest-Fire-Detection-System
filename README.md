# Forest-Fire-Detection-System
This project uses IoT sensors and a deep learning algorithm (CNN) to detect and confirm forest fires.

## Sensors Used
  - Arduino (NodeMCU32): NodeMCU is a low-cost open source IoT platform. It initially included firmware which runs on the ESP8266 Wi-Fi SoC from Espressif Systems, and hardware which was based on the ESP-12 module. Later, support for the ESP32 32-bit MCU was added.
    <br> <img src="https://user-images.githubusercontent.com/72027411/211216615-cd1a5596-9174-443e-8753-99af3d9abbe0.jpg" width="110" height="100">
  - Infrared Sensor: An infrared sensor (IR sensor) is a radiation-sensitive optoelectronic component with a spectral sensitivity in the infrared wavelength range 780 nm … 50 µm.
    <br> <img src="https://user-images.githubusercontent.com/72027411/219781449-ac07dc65-7213-4e57-be0c-0a84b80511dd.png" width="110" height="100">
  - Bulb: Lights on and off.
    <br> <img src="https://user-images.githubusercontent.com/72027411/211212492-8c49b6f3-6a92-4798-b2bd-b7157ad147d5.jpg" width="110" height="100">
  - Air Quality Sensor (MQ-135): The gas sensor module consists of a steel exoskeleton under which a sensing element is housed. This sensing element is subjected to    current through connecting leads. This current is known as heating current through it, the gases coming close to the sensing element get ionized and are absorbed by the sensing element. 
    <br> <img src="https://user-images.githubusercontent.com/72027411/211212487-d883dd8d-f80c-4902-8985-c293630f2153.jpg" width="110" height="100">
  - Buzzer: The flexible ferromagnetic disk is attracted to the coil when the magnetic field is activated, then returns to rest when the magnetic field is off. By oscillating the signal through the coil, the buzzer produces a fluctuating magnetic field, which vibrates the disk. This movement makes the buzzer sound.
    <br> <img src="https://user-images.githubusercontent.com/72027411/211212502-3d92abbe-0f13-42a0-acff-27a8c9bad98c.jpg" width="110" height="100">   
  - Temperature & Humidity Sensor: Humidity sensors work by detecting changes that alter electrical currents or temperature in the air. There are three basic types of humidity sensors: capacitive, resistive and thermal. All three types will monitor minute changes in the atmosphere in order to calculate the humidity in the air.
    <br> <img src="https://user-images.githubusercontent.com/72027411/211212473-0d4b7ab9-c83b-475b-9664-1e1d45b2b85f.png" width="110" height="100">

## Working
  We have used three sensors, a **Temperature and Humidity sensor**, an **Infrared sensor** and a **Smoke sensor**. If any two raise an alert the camera turns on, sending the pics to google drive through a google app script. The google app script is what connects the Arduino and google drive where we run our deep learning algorithm (CNN). 
The camera turns on only when any two sensor raises a high alert to reduce power consumption. We are also running CNN on the pictures uploaded by the camera, when CNN confirms the fire only then the buzzer runs alerting the respected authorities.

## Pre-requisites
  - Install the latest version of python.
  - Install all the libraries require by the Aduino Code.
  - Create google account.

## Screenshot 
![Screenshot 2023-02-19 105015](https://user-images.githubusercontent.com/72027411/219924560-1e26a166-494d-4f24-81fa-44ac9be7ce5b.png)


## Runing the project
  - **GOOGLE APPSCRIPT**
    - Start Scripting -> New Project -> Copy & paste the ESP32cam.json -> Save -> Publish -> Deploy as web app.
  - **ARDUINO IDE**
    - Copy the script URL and replace it with the myScript URL.
    - Change the ssid and password.
    - Select the board -> Upload the code
  - **GOOGLE DRIVE**
    - After the fire get detected by the sensors the images will be uplaoded to the drive.
  - **GOOGLE COLAB**
    - Run the CNN on the uploaded images to confirm the fire.
 

# Forest-Fire-Detection-System
This project is an attempt to use convolutional neural networks (CNN) to detect the presence or the start of a forest fire in an image. The idea is that this model
could be applied to detect a fire or a start of a fire in a forest. The model could be applied in real-time and give alert in case of fire.


## IoT Sensors used
### Temperature & Humidity Sensor (DHT11)
To measure the change in humidity and temperature.

### Gas & Smoke Sensor (MQ-2)
This sensor will detect the smoke produced by fire.

### Infrared Flame Sensor
This sensor detects IR light wavelength between 760 nm – 1100 nm 
that is emitted from the fire flame or light source.

### Camera (ESP32)
To click the photos, when sensors detects fires.

### Buzzer
TO alert the officials.

# How we get there :

## Sensors
The DHT11, MQ-2 and IR Flame 
sensors, if any 2 of them send a 
high alert, 
the ESP32 will start clicking the 
photos of the surroundings and 
send them to Google Drive.

## Algorithm
In Google drive we will run our 
pre-trained deep learning 
algorithm CNN (Convolutional 
Neural Network),
This help us confirm the fire and 
run the buzzer back at main 
station.

## Alert
Here, we will alert all the people 
through alert SMS, 
Also, operators can see the 
readings, photos and all data 
using an IoT support cloud 
application, that can be used to 
digitally represent the data and 
analyze it like ThingSpeak.

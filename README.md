# IOT_Project_2022
Final project for the Internet Of Things course, 2022 edition, University of Genoa (Italy)

Authors: Manuel Parmiggiani (Student ID S4701853), Giacomo Garbarino (Student ID S4545532)

The aim of this project is to define the architecture and a demo implementation of a SmartGarden environment.

The scripts contained in this repository can be used to simulate the typical execution we would expect to observe in a real SmartGarden: real-time data is collected by ad-hoc sensors and is sent to a local server through MQTT, then all of the informations have to be forwarded to a central DB in order to be available for data visualization and analysis tasks.

Each Garden has one MQTT server, one MQTT subscriber and at least two sensors.
Each Garden has its own unique topic and sensors from that Garden run scripts that were set to send data to that specific topic only.
Messages sent from sensors to the server are cached by the MQTT subscriber, which proceeeds to write them on a DB (NB: we simulated the hypothetical DB table with a txt file).



Quick summary of the scripts associated with each Garden:

-First Garden: Garden01.js Subscriber01.js Sensor01.js Sensor02.js

-Second Garden: Garden02.js Subscriber02.js Sensor03.js Sensor04.js

-Third Garden: Garden03.js Subscriber03.js Sensor05.js Sensor06.js

-Fourth Garden: Garden04.js Subscriber04.js Sensor07.js Sensor08.js

-Fifth Garden: Garden05.js Subscriber05.js Sensor09.js Sensor10.js

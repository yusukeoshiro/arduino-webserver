# Arduino IR Remote

### Things to build
* Circuit board for IR Receiver / Emitter
* Embedded program for arduino in C
* Heroku app
* Mobile app for iOS and Android

----

### Cuircuit board for IR Receiver / Emitter
Simple breadboard circuit that can connect directly to Arduino's I/O ports.

### Embedded program for Arduino
This program does the following:
* It captures the IR signal and records (persists) the captured signal to the cloud.
* Receives the signal emission request from the cloud and plays it with the IR emitter.


### Heroku App
* Records the captured signal in cloud hosted database
* Handles requests from mobile app (Only from outside local area network)
* Sends signal emission request to arduino app

### Mobile App for iOS and Android
* In local area network
 * Sends signal emission request directly to arduino app
 * Sends signal record request directly to arduino and sends record request to heroku app
* Outside local area network
 * It will send request to heroku if it is _outside_ the local area network through the internet

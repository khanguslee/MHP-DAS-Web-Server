# Monash Human Power - Data Acquisition System Web Server 

**REPO IS NOW OUT OF DATE, UPDATED CODE HERE: https://github.com/Monash-Human-Power/MHP-DAS-Web-Server**

A web server for the Data Acquisition System (DAS) for Monash Human Power.

The node.js + Express HTTP REST server is used to host the real-time dashboard whilst the MQTT broker is used to transfer data from the sensors to all the necessary scripts that need it.
 
## Getting Started
1. `npm install` to install all dependencies and libraries
2. `npm run build` when it's your first time running the application
3. `npm start` to start the server



## Documentation
Base URL: http://das-web-server.herokuapp.com

|Endpoint|Method|Body|Description|
|--------|------|----|-----------|
|/start|POST|{"filename" : *data_YYYY_MM_DD_HH_MM_SS* }|Notify server that a new data recording session has started|
|/result|GET||Returns current sensor data|
|/result|POST|TODO|Data to be stored within the specified csv file|
|/result/all|GET||Returns all sensor data|
|/files|GET||Returns an array of files that are stored on the server|
|/files/recent|GET||Download most recent file edited from server|
|/files/*filename*|GET||Download specified file from server|
|/files/*filename*|DELETE||Delete specified file from server|
|/server/status|GET||Status of the server|

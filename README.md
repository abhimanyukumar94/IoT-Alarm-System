# IoT-Alarm-System
IoT Alarm System connected to IBM Bluemix Cloud which sounds an alarm when the Light Intensity/Temperature exceeds a certain threshold

# Components used
1. TI's MSP432P401R Launchpad Development Kit
2. TI's CC3100 Module BoosterPack
3. TI's Educational BoosterPack MKII
4. IBM Bluemix IoT Service
5. IBM Blumix NODE-RED Application

# Description
1. Using the Luminosity and Temperature sensor on MKII, the MSP432 collects the Light Intensity and Temperature readings of the environment. 
2. MSP432 then sends the data to the IBM Bluemix IoT Service, using CC3100 Module, where the device is registered.
3. The IoT Service is connected to a Cloud Foundary App on Bluemix, which runs the NODE-RED application.
4. The NODE-RED application receives the data from the service and checks whether the data exceeds a certain threshold. If it does not, nothing happens.
5. If it does, then the NODE-RED application sends an alert warning to MSP432.
6. The alert warning triggers an alarm (buzzer, Imperial March tune) on MKII. 


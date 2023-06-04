# esp_master

** Equipment used:
- ESP8266
- Ultrasonic Sensor - HC-SR04

** Build system:
- Master - ESP8266:
+ Receives garbage detection signal from sensor HC-SR04.
+ ESP8266 uses web socket protocol to send face and garbage capture signals to 2 phones.
+ After the capture is complete, the junk phone will send the label to the ESP8266 and the ESP8266 will send it to the face capture phone. Then, in the face capture phone, it will wait for the user's input signal (choose what garbage classification), conduct comparison, and finally send a signal to the ESP8266 to know which type of garbage is classified in. which side of the trash can.
+ ESP8266 communicates with Arduino Uno R3 which is connected to Shiled V3 CNC circuit using A8825 driver through I2C data exchange protocol by SDA, SCL ports.

** Thư viện sử dụng:
+ AccelStepper
+ Wire
+ ESP8266WiFi
+ ArduinoJson
+ ESP8266WiFiMulti
+ WebSocketsServer
+ ESP8266WebServer

** IDE Platform: PlatformIO + Arduino IDE

** Hướng dẫn cài đặt:
- Đối với mạch ESP8266, tải code về, tải các thư viện phù hợp, sau đó tiến hành upload code dành cho Master.

** LƯU Ý:
- Khi upload code, tháo chân cắm SDA và SCL ra, sau khi code upload xong có thể cắm vào.
- Tiến hành kết nối động cơ với mạch trước rồi mới cấp nguồn cho CNC Shield V3.

** Library use:
+ AccelStepper
+ Wire
+ ESP8266WiFi
+ ArduinoJson
+ ESP8266WiFiMulti
+ WebSocketsServer
+ ESP8266WebServer

** IDE Platform: PlatformIO + Arduino IDE

** Installation Instructions:
- For the ESP8266 circuit, download the code, download the appropriate libraries, then proceed to upload the code for the Master.

** NOTE:
- When uploading the code, remove the SDA and SCL plugs, after the code upload is complete, you can plug it in.
- Connect the motor to the circuit first and then power on the CNC Shield V3.
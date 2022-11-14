# Android-Paho-Practice
Creating MQTT Connection using MqttAndroidClient (language: java)

Being different from MqttClient java package, MqttAndroidClient works well for Android application. <br />
For the local test, you should use 'right IP address' for the application to reach out your computer server. <br />
<strong>NOTE</strong>: local server connection via '127.0.0.1' or 'localhost' is not available <br />

## :satellite: Android Networking
Instead of localhost,
you should use '10.0.2.2' to connect to your local computer server. <br />
(According to Android Developers Guide: https://developer.android.com/studio/run/emulator-networking) <br />

## :exclamation: Android Dependencies
### target Sdk version: 30 working
Currently, I have tested that MqttAndroidClient is working well at targetSdk 30(at most). <br />

## :exclamation: Server Environment
- OS: Windows
- MQTT: mosquitto <br />

## :cloud: How to setup MQTT Server at Windows OS
### 1. Download mosquitto client
- Link: https://mosquitto.org/download/
### 2. Start mosquitto server
- Open Services Application
- Find mosquitto broker and run
![Service](https://user-images.githubusercontent.com/110809138/201588396-b65dc27e-9c55-4c49-af85-35228fcddf72.png)
### 3. Setup MQTT broker, wait for 'MyTopic'
- Move to mosquitto directory: `PS> cd '.\Program Files\mosquitto\'` <br />
- Start MQTT receiver: `PS> .\mosquitto_sub.exe -t MyTopic` <br />
![Subscriber](https://user-images.githubusercontent.com/110809138/201588605-06c470c3-7d36-4eff-847f-5bd6cc6fe172.png)
<br /><br />
## :clapper: Result
- <strong>Making connection:</strong><br />
When user clicks 'connect' button, the application subscribes 'MyTopic' as topic for Mqtt message publication.<br />
- <strong>Message publication:</strong><br />
When user clicks 'publish' button, the application(publisher) will publish 'the payload' as message to mqtt server.<br />
- <strong>Disconnection</strong><br />
When user clicks 'disconnect' button, the application will disconnect from the server.<br />
<br />

https://user-images.githubusercontent.com/110809138/201592168-93b2ac92-3578-401c-b41b-961ec89faa75.mp4


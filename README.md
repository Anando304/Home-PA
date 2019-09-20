<img src="https://static.thenounproject.com/png/132885-200.png" width="200" height="200">

# Home-PA

> A SmartHome Assistant developed at HackTheNorth 2019 by Anando Zaman, Sajal Chodha, and Seeam Islam

**Overview**

In recent years, smart home systems have exploded in popularity. With different services such as Google Home and Amazon Alexa, home security has never been more accessible. Home security
and surveillance concern all homeowners, but currently, there are no effective platforms to manage different smart products without opening the product's respective proprietary app.
Home PA eliminates the need of downloading multiple apps and allows you to manage all your smart home devices in one single voice platform using Google Home or Amazon Alexa. Home-PA can help you get information 
about the last time someone opened your main door, status of backyard motion (if a motion detection camera is installed) and much more!

**TECHNICAL ASPECTS**

- Languages used: Python 3.5

- Database: Google Firebase and Python Flask Server

- Authentication: Google Firebase API

- Chatbot: Google DialogFlow and Facebook Messenger APIs

- Hardware/Sensor systems: Arduino and breadboard circuits

**How to setup**

1. Clone the repository and open Arduino-Sensor Python folder. Compile and upload the ArduinoPythonRead.ino code to your Arduino UNO. (Make sure you remember which COM port it is connected to)

2. Open ArduinoPythonRead.py script and navigate to line 27 with the serial COM ports. Rename 'COM3' to the one you made note of earlier.

3. Save and run the script at all times. This will constantly read for changes in the Arduino inputs.

4. Navigate to DialogFlow folder and launch ngrok.exe. Type in the following command
```
ngrok http 8888
```
5. This generates a ngrok url. This activates the ability for POST/GET requests to be sent from Dialogflow to the Flask server via DialogFlow webhook to the auto-generated ngrok url.

6. Copy and paste this to DialogFlow fullfillments webhook section.

7. Run 'Dialog.py' and have it running at all times. This will be the Flask server that is responsible for getting POST/GET requests from dialogflow and creating an appropriate response.

**Sample Conversation**
<div>
  <div style="float:left;">
    <a href="https://www.kapwing.com/videos/5d7ed58448de030013c4b95d"><img src="https://i.ibb.co/hXVt3TZ/HomePA.png" width="300" height="680"></a> 
  </div>
</div>

<a href="https://www.kapwing.com/videos/5d7ed58448de030013c4b95d">Check it out!</a>


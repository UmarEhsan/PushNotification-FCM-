# PushNotification-FCM-

#Ionic Push Notification
Create a new ionic project<br>
ionic start push-notification blank<br>
navigate to your project (cd push-notification)<br>
Add this plugin <br>
ionic add ionic-platform-web-client <br>
Now you need to get your senderID of your firebase base project <br>
Go to firebase console (https://firebase.google.com/) and create a new project <br>
Get your senderID from Project Settings of your firebase project <br>

<p align="center">
  <img src="firebase-console.PNG" width="350"/>
  
</p>

Inside Cloud Messaging tab you can get your senderId <br>
<p align="center">
  <img src="Sender-id.PNG" width="350"/>
  
</p>
<br>
Now we get our senderId from our firebase project add phonegap-plugin-push with your senderId
ionic plugin add phonegap-plugin-push --variable SENDER_ID="SENDER_ID of your project"

Alright, the basic is done, let’s connect our app to the <a href="">Ionic.io</a> services!

If you have no account there, now is the time. It’s free and you need it in order to send Ionic push notifications to your app.

After creating your ionic.io account then continue on your command line and run:
ionic io init
ionic config set dev_push true

First of all this will create an app id inside your Ioni.io dashboard, and we also enable Dev Pushes for our app to test if everything works until now.
Open up your app.js and replace the current .run() block with this:

<p align="center">
  <img src="run.PNG" width="350"/>
  
</p>
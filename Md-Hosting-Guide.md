# Md Bot Heroku Deploy Guide

<b><details><summary>⚠ Requirements</summary></b>

 - [MongoDB](https://www.mongodb.com)
 - [Heroku](https://heroku.com)
 - Another Phone/Device to scan qr
```bash 
Sign in/up to Heroku and MongoDB
```
</details>

1. Go to [MongoDB cloud atlas](https://www.mongodb.com/cloud/atlas)

2. Sign up if you don't have an account already or log in if you have one already.
PS: If you don't want to use your email, go to https://temp-mail.org/en/ and generate a temporary disposable email address uwu)/
3. Create a new cluster on Mongo Atlas. [It takes time, so don't worry]
4. After creating a cluster, click on the 'CONNECT' button on the cluster which you've created.
5. On Setup connection security, I'd recommend you to add 'Your Current IP Address' for security concerns but if you are not willing to go through a little bit of pain, then simply add 'Access from anywhere. Also, you can change this anytime by opening your "IP Access list tab".
6. Then, create a database user, fill up the name and password and MAKE SURE TO REMEMBER THEM.
7. Click on the "Choose a connection method" and then click on the "Connect Your Application" option.
8. Finally, on the "Connect" tab select "Nodejs" as _DRIVER_ with "3.6 or later" in _VERSION_.
9. Copy the connection string that is provided below and paste it somewhere and replace <password> with 'the password you added while creating database user', also make sure to remove '< >' these from <yourPassword>. This will be your _MONGO CLUSTER URI_.
#### Example [Mongo Atlas Cluster URI]
```mongodb+srv://NekoDaKamiSama:kamisamaofdaculture@cluster0.v93qb.mongodb.net/myFirstDatabase?retryWrites=true&w=majority```

10. That's it You now have a MongoDB cluster hosted on Mongo-Atlas. You can use this cluster for other projects too.

### Pre-requisite

1. [WhatsApp-bot](https://github.com/LuckyYam/WhatsApp-bot) - Go there
2. Scroll down a bit and you will see the "Deploy To Heroku" button in purple color (sorry if you are color blind)
3. Click on it and login or sign up for Heroku
4. Enter the following fields
    | KEY | VALUE |
    | --- | ----------- |
    | NAME | NAME_OF_THE_BOT |
    | PREFIX | PREFIX_OF_THE_BOT |
    | SESSION | BOT_SESSION |
    | MODS | BOT_ADMINS_NUMBER (should be seperated by a comma and a space) |
    | MONGO_URI | YOUR_CLUSTER_URI |
 - `PREFIX`: Prefix of the bot
 - `BOT_NAME`: Name of the bot
 - `MONGO_URI`: A secret String for MongoDB connection. (Required)
 - `MODS`: Number of the users who should be the admins of the bot (should be in international format without "+" and multiple numbers should be separated by a comma  and a space). Example - 1234567890, 91245670325 (you shouldn't add "@s.whatsapp.net" at the end of each numbers)
 - `SESSION`: Session of the bot
5. Wait for the building to finish, you should always keep an eye on log messages, you can find log messages in the Dashboard -> More -> View logs.<br>
6. After it builds, click on the "View" or "Open App".<br>
7. Authenticate By Providing Your SESSION_ID and a QR Code Will Show Up.<br>
8. Open WhatsApp on your phone -> Click on the 3 Dots on the top Right -> Click on WhatsApp Web -> Click on "Link a Device" and scan the QR from the previous step.<br>
9. Your heroku app can fall asleep so for keeping it awaken add your app to ([Kaffeine](https://kaffeine.herokuapp.com/))<br>. It pings your Heroku app every 30 minutes so it will never go to sleep.<br>

Facebook Integration with Android Facebook SDK 4.0: 

---Features: 

1) Login Facebook (with Facebook Login Button and Customized Button), check current access

2) Share Photo on Facebook

3) Get user Profile: id, name, email, birthday, profile picture

4) Get user's friend list who use this app

5) Get user's photos

---Preparation:

1) Get facebook debug key hash:

- Download openssl-0.9.8e_X64.zip on https://code.google.com/archive/p/openssl-for-windows/downloads

- Extract the file to folder to C:\OpenSSL

- Find the debug.keystore file path (It is in folder C:\Users\%UserName%\.android)

- At the path: C:\Program Files\Java\jre1.8.0_65\bin, open cmd and paste the following code:

keytool -exportcert -alias androiddebugkey -keystore C:\Users\%UserName%\.android\debug.keystore | C:\OpenSSL\openssl sha1 -binary | C:\OpenSSL\openssl base64

2) Get facebook release key hash:

- Follow the instruction on https://developer.android.com/studio/publish/app-signing.html to get the release key app (.jks file)

- Notice to put an alias name to your release key

- At the path: C:\Program Files\Java\jre1.8.0_65\bin, open cmd and paste the following code:

keytool -exportcert -alias yourappreleasekeyalias -keystore ~/.your/path/release.keystore | C:\OpenSSL\openssl sha1 -binary | C:\OpenSSL\openssl base64

--- Reference and More Information:

https://developers.facebook.com/docs/android/getting-started

https://developers.facebook.com/docs/facebook-login/android

http://stackoverflow.com/questions/13896892/facebook-sdk-3-0-android

http://stackoverflow.com/questions/29295987/android-facebook-4-0-sdk-how-to-get-email-date-of-birth-and-gender-of-user

http://stackoverflow.com/questions/29491479/fetch-friends-list-from-facebook-sdk-4-0-1-in-android-with-graph-api-2-2

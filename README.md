This is a starter template for [Ionic](venkat)projects.

## How to use this template

*Download the files
https://github.com/venkatch668/ionic2.git

### With the Ionic CLI:
Take the name after `ionic2-`, and that is the name of the template to be used when using the `ionic start` command below:

```bash
$ npm install -g ionic cordova
$ ionic start myTabs tabs
```

Then, to run it, cd into `myTabs` and run:

```bash
$ ionic cordova platform ios or $ ionic cordova platform andorid
$ ionic cordova run ios or $ ionic cordova run andorid
```

## Ionic Setup & Deploy
<ol>
	<li><p>Install Ionic and coredova files</p> 
		<p><b>Command :</b> npm install -g cordova ionic</p>
		<p><b>Ref:</b> http://ionicframework.com/getting-started/</p>
	</li>
	<li>
		<p>Develop your own login / application as per requirement</p>
	</li>
	<li><p>Install Latest Android SDK(2.3), Java Latest version (1.8)</p>
		<p><b>Ref:</b> https://developer.android.com/studio/index.html</p>
		<p><b>Ref:</b> https://www.java.com/en/download/windows-64bit.jsp</p>
		<p>Set proper environment variables</p>
		<p>1.	JAVA_HOME</p>
		<p>2.	Path</p>
	</li>
	<li><p>Get Setup/build ready</p>
		<p><b>Command:</b> ionic cordova run android --prod –release</p>
		<p>Then it will create unsigned .apk file in below path</p>
		<p><b>Path:</b> myApp\platforms\android\build\outputs\apk</p>
		<p>But to install in device we need signed .apk</p>
	</li>
	<li><p>Sign Android APK</p>	
		<p><b>Command:</b>  keytool -genkey -v -keystore my-release-key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias my-alias</p>
		<p><b>Enter password:</b> demoadmin123 & re-enter again (Note: we can use any password, we should use same password in whole app)</p>
		<p><b>Command:</b> jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore my-release-key.jks android-release-unsigned.apk my-alias</p>
		<p>Enter password: demoadmin123</p>
		<p><b>Ref:</b> http://ionicframework.com/docs/intro/deploying/</p>
	</ol>
	<h3>Now Signed .apk file is ready, copy into mobile then install.</h3>

	<p><b>Additional Points:</b></p>
	1.	Need 5 hours of time to setup
	2.	Good internet speed
	3.	Careful on setup javapath

@venkat 
# Flutter Demo

Fully working firebase Flutter app with authentication and CRUD.
Instructions and tests are only done on Android at the moment,
as I dont own a mac or iphone.
I am avaialble for business and knowledge sharing. Hit me up

ps: This code base is clean as and it gets cleaner by the day
## Some Screenshots
<div>
<img src="https://imgur.com/ZASwk0x.jpg" alt="Login" width="200"/>
<img src="https://imgur.com/4TJK8LH.jpg" alt="Register" width="200"/>
<img src="https://imgur.com/ApX2iB9.jpg" alt="Home" width="200"/>
</div>
<div>
<img src="https://imgur.com/s41c9qU.jpg" alt="Create Crud" width="200"/>
<img src="https://imgur.com/Vre3Mxb.jpg" alt="App Drawer" width="200"/>
</div> 


## Getting Started

* Install flutter on your machine
* `git clone https://github.com/MMHossaini/Flutter.git`
* `cd Flutter`
* Download the generated `google-services.json` from firebase project and place it inside `android/app`. 
* `flutter run`


## Features

* Login
* Registration
* Reset Password
* Onboarding Page
* Global error handler
* Fully Working CRUD example


# Publishing(Deploying to palystore and ios store)

This app , This exact repo is published to google paly store if you search for `Apps Factory`, not ios store yet. 
IF you want to use this project as your starting point project and makes changes to, then i say choice! and here are thee instructions for you to make it visible to world.

## Android 
You need to sign your app first of all

### icon
Set the path to your app icon in `pubspec.yaml flutter_icons: image_path: <yourAppIconPathHere>`

Now run `flutter pub run flutter_launcher_icons:main`
This will replace all the default flutter app icons in your app to your new image, you can check this into your repo but i have not because i want you to really try it your self. when this project was first created with `flutter create app` it came with default icons and this repository contains the default icons. I also update the icon when i deploy my app to playstore. 

### Signing the app
Create a key 

`keytool -genkey -v -keystore c:/path/to/your/key.jks -storetype JKS -keyalg RSA -keysize 2048 -validity 10000 -alias key
`

Open and update `\android\key.properties` file values

Build an app bundle
`flutter build appbundle`

IF successfully built, you will get a file `build\app\outputs\bundle\release\app.aab`

You should test your app bundle before deploying to play store

download bundletool from the GitHub repository.

`java -jar bundletool-all-0.11.0.jar build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks --ks=/MyApp/keystore.jks--ks-pass=file:/MyApp/keystore.pwd--ks-key-alias=MyKeyAlias --key-pass=file:/MyApp/key.pwd`

Generate a set of APKs from your app bundle.
Deploy the APKs to connected devices.
`bundletool install-apks --apks=/MyApp/my_app.apks`

If your apk from your bundle works. then you are production ready.
This repo already adds progaurd for you.s
Now you can upload your app bundle to playstore after you pay play store developer regisreration fee. Cost $25 US dollars
For more information you can check out this [Guide](https://flutter.dev/docs/deployment/android)

### TIPS 
#### Change the app name 
Open `/android/app/src/main/AndroidManifest.xml`
Edit `android:label` . Set the name to whatever you feel like

#### Versioning
Everytime you upload new version to play store make sure to update the version code, otherwise paly store will complain
[more information here](https://stackoverflow.com/a/56970752/889376)
<img src="https://imgur.com/KbSIa13.jpg"/>

## IOS 
Coming SOON! inshallah 

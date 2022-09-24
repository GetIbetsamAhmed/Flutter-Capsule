
###### Q U I C K L I N K S
[![fluttercapsule](https://img.shields.io/badge/Contribute-Now-211F1F?logo=GitHub&logoColor=ffffff)](https://github.com/GetIbetsamAhmed/Flutter-Capsule/blob/main/README.md) 
[![HEALTH](https://img.shields.io/badge/FLUTTER-HEALTH_STATUS-64DD17)](#flutter-health-status) [![Ibtesam Ahmed](https://img.shields.io/badge/FLUTTER-CREATE-304FFE)](#create-app) [![Ibtesam Ahmed](https://img.shields.io/badge/FLUTTER-RUN-2962FF)](#run-app)

## Flutter Health Status
_Run this command to check Flutter Status on your device_
```bash
flutter doctor
```
 _Run this command to check available devices for Flutter_
```bash
flutter devices
```
 _Run this command to upgrade Flutter_
```bash
flutter upgrade
```
 _Run this command to configure Flutter_
```bash
flutter config
```
 _Run this command to check Flutter Channel_
```bash
flutter channel
```
 _Run this command to switch to Flutter Channel Beta, likewise you can switch back to_ `stable`
```bash
flutter channel beta
```
 _Run this command to Repair Pub Cache_
```bash
flutter pub cache repair
```
[![TOP](https://img.shields.io/badge/Goto-Top-000000)](#q-u-i-c-k-l-i-n-k-s)
## Create App
_Run this command to create an app, just replace `app_name` with your desired app name but without spaces and special characters except_ `Underscore(_)`
```bash
flutter create app_name
```
#### Specify Package Name
_Create your Flutter app with this command to customize your app's package name; Package name from the below command will be_ `com.company.app_name` _You can change it accordingly_ 
```bash
flutter create --org com.company app_name
```
#### Create Command for Release
```bash
flutter create --androidx -t app --org com.company -a kotlin -i swift app_name
```
[![TOP](https://img.shields.io/badge/Goto-Top-000000)](#q-u-i-c-k-l-i-n-k-s)
## Run App
_Run this command to run a Flutter Project_
```dart
flutter run
```
_Run this command to check runner logs while running_
```dart
flutter run -v
```
_Run this command to run the project on specific device when there are muliple devices available replace_ `device_ID` _with your device ID_
_Sample: `flutter run -d chrome` to run flutter web project on Chrome Browser_ 
```dart
flutter run -d device_ID
```
_Run this command to run the flutter web project on specific port of localhost_
_Sample: `flutter run -d chrome --web-hostname localhost --web-port 8080` to run flutter web project on port `localhost:8080` on Web Browser_ 
```dart
flutter run -d chrome --web-hostname localhost --web-port [port_number]
```
[![TOP](https://img.shields.io/badge/Goto-Top-000000)](#q-u-i-c-k-l-i-n-k-s)
## Signing App
### Step 1
**Create a keystore**
If you have an existing keystore, skip to the next step. If not, create one by running the following at the command line:
```bash
./keytool -genkey -v -keystore ~/key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias key
```
**OR** _Run this if get error_
```bash
.\keytool -genkey -v -keystore ~/key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias key
```
**Note:** Keep this file private; do not check it into public source control. 
**Note:** keytool may not be in your path. It is part of the `Java JDK`, which is installed as part of Android Studio. For the concrete path, run `flutter doctor -v` and see the path printed after `Java binary at:` and then use that fully qualified path replacing java with keytool.

### Step 2
Reference the keystore from the app Create a file named **key.properties**`<Project>/android/key.properties` that contains a reference to your keystore: 
Add these lines in `/android/key.properties`
```properties
storePassword= password from previous step
keyPassword= password from previous step
keyAlias= key
storeFile= location of the key store file, e.g. /Users/username/key.jks
```
### Step 3
_Add these lines above android{ } (near line 16) in `/android/app/build.gradle`_
```gradle
def keystorePropertiesFile = rootProject.file("key.properties") 
def keystoreProperties = new Properties() 
keystoreProperties.load(new FileInputStream(keystorePropertiesFile)) 
```
_Add these lines in android{ }  in `/android/app/build.gradle`_
```
signingConfigs { 
	release { 
	keyAlias keystoreProperties['keyAlias']
	keyPassword keystoreProperties['keyPassword']
	storeFile file(keystoreProperties['storeFile'])
	storePassword keystoreProperties['storePassword'] 
	} 
} 
buildTypes { 
	release { 
	signingConfig signingConfigs.release 
	} 
}
```
## Add Font
We can add a new font through assets in this application
```bash
Add font .ttf in your font folder inside the assest 
```
#### Specify Package Name
_Create your Flutter app with this command to customize your app's package name; Package name from the below command will be_ `com.company.app_name` _You can change it accordingly_ 
```bash
flutter create --org com.company app_name
```
#### Create Command for Release
```bash
flutter create --androidx -t app --org com.company -a kotlin -i swift app_name
```


###### Q U I C K L I N K S
[![fluttercapsule](https://img.shields.io/badge/Contribute-Now-211F1F?logo=GitHub&logoColor=ffffff)](https://github.com/GetIbetsamAhmed/Flutter-Capsule/blob/main/README.md) 
![Flutter](https://i.imgur.com/e9V2Zf7.jpg)
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

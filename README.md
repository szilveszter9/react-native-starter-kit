# React Native Starter Kit

## Requirements
* The easiest way to set up the application and join the development is to use Android Studio.
* By using Android Studio you do not have to mess with:
 * Gradle
 * `failed to find Build Tools revision 23.0.1`
 * `Failed to resolve: com.android.support:appcompat-v7:23.0.3`

### Setup Android Studio on Arch Linux
```
yaourt -S jre jdk android-studio
```

Add the following lines to your .bashrc and restart your terminal once.
```
export ANDROID_HOME=~/Android/Sdk
export PATH=~/Android/Sdk/platform-tools:$PATH
```

### Run Android Studio using a tiling window manager
If you are using dwm - or other window managers, and you'd like to run Java application that has a UI,
you'll have to add `(sleep 4 && wmname LG3D) &` to your .xinitrc just before `exec dwm`.

### Run Emulated device
Open Android Studio. Go to Tools / Android / AVD Manager. Create and start your emulated device.



## Create a project like this one
```
npm install react-native-cli -g
```
```
react-native init ProjectNameHere
```



## Install
```
git clone git@github.com:szilveszter9/react-native-starter-kit.git ReactNativeStarterKit
cd ReactNativeStarterKit
npm install
# use npm3
```



## Bundle
```
cd ReactNativeStarterKit
mkdir dist -p
react-native bundle --platform android --entry-file index.android.js --bundle-output dist/bundle.js
```



## Run

### iOS
```
cd ReactNativeStarterKit
react-native run-ios
```
* or use Xcode and open the project file ReactNativeStarterKit/ios/ReactNativeStarterKit.xcodeproj

### Android
Have an Android emulator running, or a device connected.
Otherwise you will get `com.android.builder.testing.api.DeviceException: No connected devices`
See Requirements.
```
cd ReactNativeStarterKit
react-native run-android

# some cases you will need to run
react-native start

# open localhost:8081 to check whether is responding at all
```

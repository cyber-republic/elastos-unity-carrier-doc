## Install
```
npm install --save react-native-elastos-carrier

react-native link react-native-elastos-carrier
```

## Setup
### iOS
* open xcode
* add ElastosCarrier.framework to **Linked Frameworks and Libraries** from **/node_modules/react-native-elastos-carrier/ios/Carrier** folder
* run project


### Android
add following lines to project build.gradle 
```
flatDir{
    dirs "$rootDir/../node_modules/react-native-elastos-carrier/android/libs"
}
```
under allprojects repositories block.


## Usage
```
const carrier = new Carrier('app_name', {
    // carrier callback
});
await carrier.start();
```
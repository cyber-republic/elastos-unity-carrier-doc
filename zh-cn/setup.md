## 安装
```
npm install --save react-native-elastos-carrier

react-native link react-native-elastos-carrier
```

## 配置
### 配置iOS
* 打开 xcode
* 从 **/node_modules/react-native-elastos-carrier/ios/Carrier** 目录添加 **ElastosCarrier.framework** 到 **Linked Frameworks and Libraries**
* 运行


### 配置Android
添加以下代码到项目的 build.gradle 的 allprojects repositories 区域.
```
flatDir{
    dirs "$rootDir/../node_modules/react-native-elastos-carrier/android/libs"
}
```

## 如何开始
```
const carrier = new Carrier('app_name', {
    // carrier callback
});
await carrier.start();
```
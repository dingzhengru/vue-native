# Vue Native

*  <a href="#what-is-vue-native?">What is Vue Native?</a>
*  <a href="#installation">Installation</a>


## What is Vue Native?
**Vue.js => Vue Native => React Native**   
**Vue Native 依賴於 React Native，實際上，所有的.vue文件都會編譯成以.js後綴的React Native組件**  

<img src="https://i.imgur.com/3orw71q.png" height="200">
參考: https://vue-native.io/docs/index.html  

## Installation

## For Expo users
```
npm install --global expo-cli

vue-native init <projectName>
```
app.json  
```
{
  "expo": {
    "name": "Your app's name",
    "platforms": [
      "ios",
      "android",
      "web"
    ],
    "version": "1.0.0",
    ...
    "packagerOpts": {
+     "sourceExts": ["js", "json", "ts", "tsx", "vue"],
      "config": "metro.config.js"
    }
  }
}
```
Run the app
```
cd <projectName>
npm start
```
或是指定平台  
```
npm run ios
npm run android
```
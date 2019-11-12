# Vue Native

*  <a href="#what-is-vue-native?">What is Vue Native?</a>
*  <a href="#開始之前">開始之前(before start)</a>
*  <a href="#installation">Installation</a>

## What is Vue Native?
**Vue.js => Vue Native => React Native**   
**Vue Native 依賴於 React Native，實際上，所有的.vue文件都會編譯成以.js後綴的React Native組件**  

<img src="https://i.imgur.com/3orw71q.png" height="200">
參考: https://vue-native.io/docs/index.html  

## 開始之前
1. 開啟手機的**USB偵錯模式**```設定 > 關於裝置  > 軟體資訊 > 版本號碼 連續按7次```
2. 將手機連結電腦後，之後會執行下面的```npm start```會有QR code可以掃(掃下去會幫你安裝expo)
3. 專案開出來之後，expo會優先判定app.js為入口檔案，所以先**將app.js刪除**，就會將app.vue當入口了
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
npm start or expo start
```
指定平台  
```
npm run ios
npm run android
```

## 建立apk,ipa
**另一個視窗要執行著```npm start``` or ```expo start```時**
同時執行以下指令才會成功  
```expo build:android```  
```expo build:ios```  
執行成功後可以到expo官網 => View IPA/APK builds => 等待建立完成即可下載  

**會遇到的錯誤**
1. Set EXPO_DEBUG=true 在專案路徑直接輸入 ```Set EXPO_DEBUG=true```

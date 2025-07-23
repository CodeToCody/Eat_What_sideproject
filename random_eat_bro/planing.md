# APP專案開發

- Flutter 3.32.4 - stable
路徑:E:\APPDev\flutter\bin\flutter.bat

- 跑 ```flutter doctor``` 看一下我有啥
```
[✓] Flutter (Channel stable, 3.32.4, on Microsoft Windows [版本 10.0.19045.5965], locale zh-TW)
[✓] Windows Version (10 教育版 64-bit, 22H2, 2009)
[✓] Android toolchain - develop for Android devices (Android SDK version 35.0.0)
[✗] Chrome - develop for the web (Cannot find Chrome executable at .\Google\Chrome\Application\chrome.exe)
    ! Cannot find Chrome. Try setting CHROME_EXECUTABLE to a Chrome executable.
[!] Visual Studio - develop Windows apps (Visual Studio Build Tools 2022 17.14.5)
    ✗ Visual Studio is missing necessary components. Please re-run the Visual Studio installer for the "Desktop
      development with C++" workload, and include these components:
        MSVC v142 - VS 2019 C++ x64/x86 build tools
         - If there are multiple build tool versions available, install the latest
        C++ CMake tools for Windows
        Windows 10 SDK
[✓] Android Studio (version 2024.2)
[✓] Connected device (2 available)
[✓] Network resources
```


## 功能

1. 一個開始探索按鈕
2. APP 啟動GPS，取得目前位置
3. 使用者輸入距離(如:1km內)
4. 隨機挑一間，顯示:
    - 名稱
    - 評價
    - 地址
    - 地圖標示 and 導航

## 工具安裝與練習

1. 安裝 Flutter 開發環境（我可以一步步帶你）

2. 學會建立一個簡單的 Flutter App

3. 學會加一個按鈕、輸入欄位與地圖畫面

## 功能拆解學習
1. GPS 取得位置：geolocator 套件

2. Google 地圖顯示：google_maps_flutter 套件

3. 呼叫 Google Places API 拿附近餐廳

4. Dart 隨機選擇一間

5. 顯示地圖與資訊

## 包裝與發佈


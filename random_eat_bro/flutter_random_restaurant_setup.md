# Flutter App 開發筆記：隨機餐廳推薦器

📅 日期：2025-06-19  
🧑‍💻 開發者：自己  

---

## ✅ 專案目標

開發一個能在 iOS / Android 上運行的 App：

- 取得 GPS 位置
- 輸入距離
- 透過 Google Map 隨機推薦附近餐廳

---

## 📁 專案結構與基本操作

```bash
cd random_eat_bro
code .
flutter pub get
flutter run -d emulator-5554
```

## ✅ 2025 6/19進度紀錄

### 🔧 環境設定

- ✅ 安裝 Flutter SDK 並設好環境變數（D:\APPdevelop\Flutter_SDK\flutter）
- ✅ 安裝 Android Studio、Android SDK、AVD 模擬器
- ✅ 成功執行 `flutter doctor` 並確認模擬器可用

### 📱 模擬器設定與執行

- ✅ 建立並啟動 Android 模擬器（Pixel 型號，API 35）
- ✅ 使用 `flutter run -d emulator-5554` 成功執行 App 至模擬器

###  GPS 功能實作

- ✅ 安裝 geolocator 套件
  - 在```pubspec.yaml```檔案裡面```dependencies```裡加```geolocator: ^11.0.0```，並執行```flutter pub get```
- ✅ 修改 `AndroidManifest.xml` 權限（fine/coarse location）
- ✅ 撰寫 Flutter 程式碼實作按鈕點擊後取得目前 GPS 位置
- ✅ 顯示目前位置的緯度與經度



## 📌 待辦清單（下一步）

- [ ] 加入 Google Maps 顯示目前位置
- [ ] 串接 Google Places API 搜尋附近餐廳
- [ ] 實作隨機選取一間餐廳並顯示資訊
- [ ] 強化 UI（加入距離輸入欄位、顯示選中餐廳名稱與地圖位置）

---

## 📒 備註與錯誤處理紀錄

- ⚠️ 初始無法執行 `flutter` 指令 → 解決方式：重新下載 Flutter 並設環境變數
- ⚠️ build.gradle.kts 出現 NDK 錯誤 → 解法：從 SDK Manager 安裝 NDK 26.3.11579264
- ⚠️ symlink 錯誤提示 → 解法：不管他

---

## 💬 常用指令

```bash
flutter doctor             # 檢查環境
flutter pub get            # 安裝/更新套件
flutter run -d emulator-5554  # 指定在模擬器上執行
flutter clean              # 清除快取並重新建置
```
---

## ✅ 2025-06-19 更新：GPS 功能完成 🎯

- ✅ 成功透過 geolocator 取得模擬器預設位置（顯示十進位經緯度）
- ✅ 解析結果確認格式正確，預設值為 Google 總部位置（37°25'19.2"N 122°05'02.4"W）
- ✅ 已完成 geolocator 權限檢查與錯誤處理流程
- ✅ 若需轉換為 DMS 格式，可使用自訂函數 `decimalToDMS` 實作
- ✅ 模擬器測試已成功顯示按鈕與座標

> 下一步已確定將實作 Google Maps 地圖畫面，今日暫停在這階段

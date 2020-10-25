---
title: "Excel 分裂式圓餅圖"
date: 2019-10-29T10:07:47+06:00
draft: false

# post thumb
image: "images/featured-post/post-1.jpg"

# meta description
description: "Excel 分裂式圓餅圖"

# taxonomies
categories:
  - "Tutorial"
tags:
  - "Excel"
  - "Plot"
  - "Data"
  - "Visualization"
  - "Gene"

# post type
type: "featured"
---

圓餅圖是呈現數據中各個類別比例的好方法，但是當類別超過三個的時候，圓餅圖的呈現方式反而有可能造成誤導。這種時候最好改用長條圖或是分裂圓餅圖。

---

### 前言

使用 Excel 畫圓餅圖應該很基本，可是有些細節要調整的時候總是令人崩潰～

這次以轉錄因子家族預測結果資料做示範，將使用到簡單的樞紐分析以及調整分裂圓餅圖的分裂門檻。下圖為資料的初始樣貌，我們的目標是將第二個 column 中的 NAC、EIL、FAR1、HSF 等等轉錄因子家族名稱，利用樞紐分析自動計算出現次數，之後化成分裂圓餅圖，並依據需求調整分裂的門檻。

![https://res.cloudinary.com/rna-sick/image/upload/v1557476528/TFDB/9_mjglar.png](https://res.cloudinary.com/rna-sick/image/upload/v1557476528/TFDB/9_mjglar.png)

initialFormat

### 用樞紐分析計算出現次數

1. 先確認要統計出現次數的欄位有沒有 column 名稱。在預測結果上方插入一個 row 輸入 TF，旁邊插入一個 column 輸入 count

    ![https://res.cloudinary.com/rna-sick/image/upload/v1557476536/TFDB/10_l0xpk0.png](https://res.cloudinary.com/rna-sick/image/upload/v1557476536/TFDB/10_l0xpk0.png)

2. 全選該 column 之後，用自動填滿功能將 count 填滿 1

    ![https://res.cloudinary.com/rna-sick/image/upload/v1557476530/TFDB/11_oyrbvg.png](https://res.cloudinary.com/rna-sick/image/upload/v1557476530/TFDB/11_oyrbvg.png)

3. 選取這兩個我們處理過的 column，點選上方 Insert 分頁中的 Pivot Table

    ![https://res.cloudinary.com/rna-sick/image/upload/v1557476536/TFDB/12_lyths0.png](https://res.cloudinary.com/rna-sick/image/upload/v1557476536/TFDB/12_lyths0.png)

4. 在喜歡的地方放這個新 Pivot Table，哪裡都可以方便就好

    ![https://res.cloudinary.com/rna-sick/image/upload/v1557476529/TFDB/13_berxuz.png](https://res.cloudinary.com/rna-sick/image/upload/v1557476529/TFDB/13_berxuz.png)

5. 在右方的 PivotTable Fields 把 count 和 TF 都勾選起來，到這一步就已經有各個類別的出現次數啦

    ![https://res.cloudinary.com/rna-sick/image/upload/v1557476529/TFDB/14_ppau5e.png](https://res.cloudinary.com/rna-sick/image/upload/v1557476529/TFDB/14_ppau5e.png)

### 繪製分裂圓餅圖，調整分割比例的門檻

1. 為了待會圖表美觀，可以先依據數量大小排個序，記得要選擇擴增選取排序範圍

    ![https://res.cloudinary.com/rna-sick/image/upload/v1557476534/TFDB/15_pepn1e.png](https://res.cloudinary.com/rna-sick/image/upload/v1557476534/TFDB/15_pepn1e.png)

    ![https://res.cloudinary.com/rna-sick/image/upload/v1557476531/TFDB/16_kl0dfh.png](https://res.cloudinary.com/rna-sick/image/upload/v1557476531/TFDB/16_kl0dfh.png)

2. 就可以畫分裂圓餅圖啦

    ![https://res.cloudinary.com/rna-sick/image/upload/v1557476535/TFDB/17_tihmcb.png](https://res.cloudinary.com/rna-sick/image/upload/v1557476535/TFDB/17_tihmcb.png)

3. 類別太多，依據 legend 顏色對照看圖其實不是很有用，所以建議把 Label 以 best fit 的方式直接標示在 pie 的旁邊

    ![https://res.cloudinary.com/rna-sick/image/upload/v1557476535/TFDB/18_d7ncw3.png](https://res.cloudinary.com/rna-sick/image/upload/v1557476535/TFDB/18_d7ncw3.png)

4. 可以由右鍵選擇 Format Data Label 來對標籤要顯示的項目微調

    ![https://res.cloudinary.com/rna-sick/image/upload/v1557476539/TFDB/19_a5chdr.png](https://res.cloudinary.com/rna-sick/image/upload/v1557476539/TFDB/19_a5chdr.png)

5. 點擊一個 Pie 的部分，右鍵選擇 Format Data Seiries，選擇第三個長條圖圖示的頁籤，可以由 Split Series By 選擇分裂的方式，下方則有一些不同的參數設定，之後微調圖面就有一張美美又很佔空間的圖可以用啦～

    ![https://res.cloudinary.com/rna-sick/image/upload/v1557490901/TFDB/20_nyibam.png](https://res.cloudinary.com/rna-sick/image/upload/v1557490901/TFDB/20_nyibam.png)

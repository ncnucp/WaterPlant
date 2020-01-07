# 監測土壤自動澆水

## 目錄
1.[組員](#第五組成員)
2.[簡介](#簡介)
3.[設備](#設備)
4.[功能](#功能)
5.[分工](#分工)

---

### 第五組成員

> 105321015 呂國丞
> 105321018 陳湘蕙
> 105321047 張瑋育

---

### 簡介

有時候會忘記澆水，為了讓它健健康康長大，因此用土壤濕度監測，如果土壤現在濕度不夠它就會自動澆水。
像夏天正中午建議不要澆水，不然會傷害到植物根部造成死亡，所以我們用溫濕度感測模組來監測環境，若當下溫度過高就不要澆水。
我們也將一天的環境溫濕度以及什麼時候澆水紀錄成一個圖檔，還有幫植物拍一張照片，並將它們寄到信箱，讓你能看到植物每一天的生長環境跟樣子。

---

### 設備

| 名稱               |數量     |來源        |
| ----------------- |:-------|:----------|
| 樹莓派             | 1      |本課堂提供   |
| 溫濕度模組          | 1      |自備        |
| 土壤濕度感測器       | 1      |自備        |
| 伺服馬達            | 1      |自備        | 
| 相機模組            | 1      |自備        |
| 杜邦線              | 數條   |自備        |
| 廢棄紙箱以及寶特瓶等  | *      |自備        |

---

### 功能

1.偵側土壤的水份是否足夠
  - 使用土壤濕度監測模組
  - 每1小時偵測一次
  - 當濕度不夠時會自動澆水

---

2.自動澆水
  - 使用伺服馬達
  - 當判斷為水份不足的時候，會用伺服馬達轉角度將瓶子下傾

---

3.拍植物一張照片
  - 用相機模組
  - 用crontab來定時拍照

---

4.將環境溫濕度、土壤濕度狀況以及澆水紀錄成一個文件檔
  ![](https://i.imgur.com/z4RWl1r.png)

---

5.將文件檔做成圖表
  - 用crontab來定時製作圖表
  ![](https://i.imgur.com/ibG53kM.jpg)

---

6.每天會傳送一份圖表以及照片到信箱，監控你植物的狀態
  - 用crontab來定時寄信
  ![](https://i.imgur.com/caDK7JL.jpg)


---


### 遇到的困難
* 土壤濕度偵測器無法直接傳輸濕度數值
    * 若是直接透過raspberry pi來接收會只剩下傳輸濕(1)跟不濕(0)這兩種值（YL-69有模擬輸出（AO口）和數字輸出（DO口），樹莓派的GPIO只支持數字輸入）


---

* gnuplot 的數值會重疊，如下圖： ![](https://i.imgur.com/igX5qys.png)

---

* 改善過後:
![](https://i.imgur.com/FZfSp7Y.png)


---

### 成品圖片
![](https://i.imgur.com/6wBteSD.jpg)

---

### 分工

* 呂國丞：主題發想，圖表製作，程式設計
* 陳湘蕙：主題發想，機關製作，報告製作
* 張瑋育：主題發想，主要程式設計，報告製作

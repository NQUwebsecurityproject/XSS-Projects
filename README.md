# 網站資安防護website-security
### 為金門大學 資訊工程學系 第五組
### 指導教授：柯志亨
### 組員：劉鳳安、陸佑函、蘇川民、王文濤、許哲瑋
## 一．專題動機
網路的時代有好的面向也有壞的面向，尤其是現代物聯網要崛起的時代。
我們的帳號和密碼到底怎麼被盜的呢?可能是"暴力破解"、"釣魚"、"封包竊取"等等可以竊取個資的方法，
我們應該要知道怎麼做防護，因為有可能因為一不小心的疏忽，讓自己的資訊被有心人士利用，所以我們要懂得怎麼保護自己的資訊，並且教導他人危機意識與防護的重要，
要怎麼做到呢？那就要在網站系統的Server上加一些防護機制，像是蜜罐誘導讓駭客困在陷阱中，又或是在防火牆上加些防護機制，等等手段來防止有心人士。
## 二．專題研究的攻擊方式
### 1.暴力破解
用Hydra套件來做暴力破解或字典攻擊，最主要是猜測帳號與密碼，把可能的選項一個個去試出來。  
主要以攻擊Webcam來做示範，可以看到設定Webcam時，要做登入的動作，所以我們猜測帳號與密碼，這樣我們就可以看到Webcam的影像。  
[暴力破解Webcam]()
### 2.釣魚網站
 「網路釣魚」 （Phishing）即為透過"不明網站"來騙取個人資料的方式，最主要是騙取帳號與密碼用，可能以以下兩種方式做為網站的背景  
 1.使用與官網相似的網址與頁面（假網頁）  
 2.網路抽獎廣告連結  
 這裡有幾種建立釣魚網站的方式：  
 [beef建置釣魚網站]()  
 [Apache建簡易網站](https://github.com/NQUwebsecurityproject/website-security/tree/master/XSS%E6%94%BB%E6%93%8A/hackpasswd/hackerproof) 
### 3.DoS,DDoS

## 三．防護機制
### 1.IPtable

### 2.Fail2ban

### 3.二次認證

---
author: jx tsai
comments: true
date: 2015-06-19 08:59:00+00:00
title: 樹莓派微電腦
wordpress_id: 132
categories:
- buy
- python
---

雖然幾年前從習慣訂閱的科技部落格消息中得知國外有出35元美金電腦，自己並未認真關注，但是今年年初從[coursera ](http://coursera.org/)線上課程「[Programming for Everybody (Python)](https://www.coursera.org/course/pythonlearn) 」上，課程講師第一週就加碼額外介紹一台信用卡片大小的微電腦接到螢幕上，就可以開始來練習寫python程式，心想太酷了，便稍花了點時間，查找網路上這台「樹莓派」小電腦的介紹資料。  
  
  
  
從谷歌大神中文結果出現前排的網站當是「Raspberry Pi台灣樹莓派」,看了上面提供的參考資源以及同好間的聚會切磋，似乎著重硬體應用的探索，讓我這個不懂任何電腦程式語言又不知電路版作用的文組魯蛇有點無從入手，有點想打退堂鼓,且當時要新上市的昇級版的Raspberry Pi 2 Model B 台灣供貨未到，我暫時打消一股買樹莓派學習寫程式的熱情XD。  
  
最近看完1987年出版的[「黑客列傳」](http://self.jxtsai.info/2015/08/where-wizards-stay-up-late.html)一書，其中生動地描寫了1970年代，第一台「家用／個人用」電腦[Altair 8800 的傳奇](http://s90304a123.pixnet.net/blog/post/33304597-%E7%AC%AC%E4%B8%80%E5%8F%B0%E5%80%8B%E4%BA%BA%E9%9B%BB%E8%85%A6altair-8800%E8%AA%95%E7%94%9F%E8%A8%98)。當時這台機子只有4K動態記憶板，沒有顯示器和鍵盤。看到40年前的阿宅們追求電子産品DIY的熱情，也激起我也想了解電腦軟硬件的好奇，畢竟如今我們已經在巨人的肩膀上享受太多的方便和習以為常，樹莓派與其說是反樸歸真之作，更是帶著人們懷著早年黑客克服軟硬技術不全，仍執意探索繼續向前各種電子機械可能的荒拓指南針。作了一點比價功課後，決定從[英商歐諾時（RS Components）的網站](http://twcn.rs-online.com/web/p/products/7568308/)上訂購樹莓派。  
  
除了「主機」外，同時購入塑膠透明外殼，搭配的USB無線網卡是另外從買自Yahoo奇摩購物中心，因為RS的Edmix價格差了快一倍。RS Components看起來像是中盤供應商，提供數量大的折扣訂單，但我這種只有零買的消費者，還是可以感受到他們細心的照顧。原本以為同時下單買了二件商品會一起裝箱送到，但下單後第二天就數收到物品（中間隔一天，且遇上週六，本以為隔週才會收到），還是二件物品分開包裝成了二筆同時送達的郵單，然後事後再收到另外二張分別寄來的發票，可見RS Components非常支持台灣郵政啊。雖然只與他們交易過一次，不過個人的體驗還蠻不錯的，幫忙廣告推薦一下。  
  
![RS Components, raspberrypi](https://4.bp.blogspot.com/-Knfs7J0SqtM/V3w_jTtxlOI/AAAAAAAAKLc/Wy0ABQaXnKcO7aPdbhZ9WXtD5yg5T-2ZwCLcB/s1600/18917678581_ec41f45ca7_z.jpg)  
  
![Raspberry Pi 2 Model B ](https://3.bp.blogspot.com/-x8Hz7ORu7to/V3w_0M5tTTI/AAAAAAAAKLg/iQ1-ZHO-b0cww4TQBA5G8IpGds-ocjmmACLcB/s1600/18727145100_3023b2fb03_z.jpg)  
  
樹莓派本身沒有外取儲存空間，故要自行搭配 micro SD card,然後去[官方網站下載作業程式](https://www.raspberrypi.org/downloads/)，從其官網上可以看到，除了樹莓派本身開發的Raspbian作業系統外，還有列有一堆第三方開發的作業系統，連快上市的微軟windows 10都可以裝在這台小機子上面。我先把手上目前僅有的一張microSD Card 用來儲解壓縮後的NOOBS檔案，它會在第一次開機時，詢問所有者要裝入哪一些作業系統。除了ubuntu 沒有列入其選項中，其它的 OpenELEC，Pidora，OSMC，RISC OS 都可和Raspbian一併安裝到micro SD card 上。  
  
![raspberrypi OS](https://4.bp.blogspot.com/-jTFUjs1MsNc/V3w_9Ih8ZxI/AAAAAAAAKLk/NeX-LIppwPE2m-6tWdpZFS47Cwep1AzRQCLcB/s1600/pyOS.png)  
  
因為樹莓派本身的輸出接口是HDMI， 我棄置已久的電腦螢幕不支援，故先把它接上了液晶電視作第一次的開機設定（記得解壓縮後的NOOBS檔案要全部複制到micro SD card的根目錄，一開始我不知道只是把整個資料夾copy到SD CARD,而非根目錄，接上電視與電源後卻沒畫面反應，還擔心這種35美元的電腦似乎不可靠啊XD）。之後我另找來HDMI to VGA 轉接頭，那台4:3的老舊LCD才能重出江湖派上用場。（其實不只是裝上轉接頭這麼簡單，還得再做一點設定檔的修改調整：排除 [Raspberry Pi 無法使用 HDMI to VGA 的問題](http://www.arthurtoday.com/2014/05/raspberry-pi-hdmi-to-vga-how-to.html)）  
![樹莓派加上老螢幕](https://1.bp.blogspot.com/-ynSF4LONfDo/V3xAEw1CX7I/AAAAAAAAKLo/2TUqB50XdvMOab9TxIOsSaFNny0AsKkpQCLcB/s1600/18728653269_d2a5b38895_z.jpg)  
  
當初産生開發樹莓派這種載裝開源系統的低價微型電腦動機，主要是希望提供便宜硬體，讓不分貧富的孩童都可以學習編寫程式，故在其官方開發的作業系統Raspbian預載了[python](http://www.python.org/), [scratch](https://scratch.mit.edu/) 這兩種據說是最受推薦的入門程式語言（後者連電腦語法都不必會）。  
  
如果問我，現在真的有好好地利用樹莓派先來學習編寫程式嗎？我的回答是：「呃，我正在利用筆電，重新回頭看之前coursera介紹scratch：[Code Yourself ](https://www.coursera.org/course/codeyourself)與python:[Learn to Program: The Fundamentals](https://www.coursera.org/course/programming1) 的線上課程XDXD」。

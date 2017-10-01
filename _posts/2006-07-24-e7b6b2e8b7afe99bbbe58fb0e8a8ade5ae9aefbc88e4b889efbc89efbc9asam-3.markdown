---
author: jx tsai
comments: true
date: 2006-07-24 02:39:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2006/07/24/%e7%b6%b2%e8%b7%af%e9%9b%bb%e5%8f%b0%e8%a8%ad%e5%ae%9a%ef%bc%88%e4%b8%89%ef%bc%89%ef%bc%9asam-3/
slug: '%e7%b6%b2%e8%b7%af%e9%9b%bb%e5%8f%b0%e8%a8%ad%e5%ae%9a%ef%bc%88%e4%b8%89%ef%bc%89%ef%bc%9asam-3'
title: 網路電台設定（三）：SAM 3
wordpress_id: 608
categories:
- dotlife
- multimedia
- software
---

[SAM Broadcaster](http://www.spacialaudio.com/products/sambroadcaster/)似乎是台灣學生網路電台界最為普遍的DJ播放軟體。 網路上流傳著[法兒電台](http://www.farradio.net/)的台柱Far大大，就錄製了一段長達20多分鐘的SAM 2示範?學影片檔案，算是很好的軟體操作入門指引。(好像不便在此轉錄該影片的位置，有心的朋友可以到PTT BBS站裏的Webradio裏找到該資訊)  
  
![]()  
  
所以我想，自己也不用再花時間嘮叨多言，只是整理一下一些提醒新手的地方。  
  
1. 在引導安裝過程中，會出現要你選擇某個資料庫的畫面。其實我也不太懂這個資料庫，和SAM的操作有什麼關聯。所以在個人電腦上，我便以較輕巧的FireBird 作為預設的資料庫和SAM互相整合。  
  
2. 聲音格式轉碼品質與網路伺服器的設定。在SAM底下的Econder設定（windows選項下的某個功能），可以設定電台伺服器的資料，如此才能把製作好的聲音傳到網路上播放。例如是用自己的PC做radio sever,，則sever IP就填入:localhost，如果是透過別人提供給你的server，就填上他所提供的IP資訊。  
  
3. 之前提過的[Listen2myRadio](http://www.formosa319.org/a5288/?p=183)就是以Shoutcast 做為其免費網路電台的伺服器協定。我發現原來除了它所指定的網址之外，其實也可以直接輸入IP和Port 資料，然後連線到該網址，就會出現其個人Shoutcast 的收聽畫面。以我申請的 a5288.listen2myradio.com 為例，開啟該網頁後，它會過五秒再自動轉址到這個用戶的電台收聽資料http://listen2myradio.com/radio.php?port=9874&ipp;=84.95.247.20 ，而這個網址所顯示的"84.95.247.20" 就是該網路電台的IP位置，port=9874。所以如果我換一個方法，打開網頁，在網址地方輸入http://84.95.247.20：9874，就同樣會看到[我的個人電台 Shoutcast](http://84.95.247.20:9874/) 的資料與收聽擊點。  
  
另外，在OSX底下也有[NICECAST](http://www.formosa319.org/a5288/?p=198)這個類似的廣播DJ軟體，至於有沒有類似SAM這種專業的DJ操作軟體，我還得花時間尋找研究一下。

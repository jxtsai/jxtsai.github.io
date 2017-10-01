---
author: jx tsai
comments: true
date: 2016-03-12 20:02:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/03/12/osmc-youtube-%e5%a4%96%e6%8e%9b%e5%95%8f%e9%a1%8c/
slug: osmc-youtube-%e5%a4%96%e6%8e%9b%e5%95%8f%e9%a1%8c
title: OSMC youtube 外掛問題
wordpress_id: 91
categories:
- multimedia
- reading /watching/ listening
---

OSMC是一款基於linux Debia發佈版本所寫成的開源媒體播放軟體,主要安裝在Apple TV, Raspberry Pi, 和自家出産的Vero 播放器上。  
  
話說自從我去年六月[買入一台樹莓派小電腦](http://self.jxtsai.info/2015/06/blog-post_19.html)後，發願要施行的python程式入門學習進展有限，這台小電腦就慢慢被冷落在一旁。直到今年初舊曆年沒什麼娛樂節目好看，久久再度打電源線接上樹莓派。  
  
當時一開始會安裝OSMC完全是透過樹莓派官網推薦的傻瓜式作業系統安裝[NOOBS](https://www.raspberrypi.org/downloads/noobs/)，在第一次開機後，系統會自動詢問用戶要安裝哪一些作業系統，包括：Raspbian， OSMC， OPENELEC， RISC OS， WIN10等c多種選項，方看使用者自己的偏好與硬碟（SD card）容量的大小。而利用OSMC在自家內部網路，也可以讀取另一台電腦所分享的檔案，如此一來，就可以在更大的螢幕與更好的音響效果下播放多媒體檔案。如果一台便宜的樹莓派小電腦，可說是擔起多媒體播放器與NAS硬碟分享的強大功能。  
![OSMC](https://3.bp.blogspot.com/-hgyrcXnuTQU/V329SFGIYYI/AAAAAAAAKSw/hIusOwFcmVgmdazK_0tpvaH7XOqforw-wCLcB/s320/step2-784x470.pn)   
  
OSMC軟體庫裏，有許多志工們貢獻寫出的外掛，進一步大大強化它的功能。例如美國知名的獨立媒體[Democracy Now](http://www.democracynow.org/), 也可以在OSMC上找到這個外掛，讓用戶可以方便地安裝後觀賞它的任何一集節目。  
  
但最近不知怎麼了，它的youtube 外掛出了點問題，當我要搜尋或試圖連上使用時，總是回應：bad request 無法開啟任何水管上的節目。雖然也有其它網路影音的外掛（例如vimeo）可以選擇，但其內容真的是比水管要少許多。雖說也是可以把多媒體影音檔案抓下來放在內部網路中的分享硬碟，但是你知道，隨著寬頻與線上觀賞的串流服務越來越方便，我就越來越少使用動物軟體。現在OSMC 水管外掛出了問題，實在是令我心悶不已。  
  
查了一下到底是出了什麼問題還是只有我一個人這麼倒楣，從[OSMC討論區的消息](https://discourse.osmc.tv/t/youtube-bad-request/13543)，方知這由於Google 更改了 API key 所以目前所有的外掛版都無法成功連接，而解決方法則是移除原有  
youthube addon，下載手動安裝[修正版的YouTube addon](http://forum.kodi.tv/showthread.php?tid=200735&page=210)。  
  
照理說，手動安裝方式有二：  
1. 在OSMC 的system 選項底下，選擇Setting/ Add-ons/install from zip file, 然後指定新下載的plugin.video.youtube.zip  
  
2. 拔下SD Card，把它接上電腦的讀卡機。在檔案管理下檢查記憶卡上原來YouTube addon的檔案位置（一般存在 /home/osmc/.kodi/addons/plugin.video.youtube)。把整個plugin.video.youtube 資料夾刪除，然後將新下載後解壓縮的plugin.video.youtube 複製過去。  
  
成功修復OSMC Youtube Add-on, 收工。繼續享受大畫面與環繞音響的線上串流。

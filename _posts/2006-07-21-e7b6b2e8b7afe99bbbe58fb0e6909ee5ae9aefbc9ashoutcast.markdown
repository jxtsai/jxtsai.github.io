---
author: jx tsai
comments: true
date: 2006-07-21 02:39:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2006/07/21/%e7%b6%b2%e8%b7%af%e9%9b%bb%e5%8f%b0%e6%90%9e%e5%ae%9a%ef%bc%9ashoutcast/
slug: '%e7%b6%b2%e8%b7%af%e9%9b%bb%e5%8f%b0%e6%90%9e%e5%ae%9a%ef%bc%9ashoutcast'
title: 網路電台搞定：shoutcast
wordpress_id: 614
categories:
- dotlife
- multimedia
- software
---

之前提過，在前辦公室搞[網路設定](http://www.formosa319.org/a5288/?p=189)，忙了半天，無疾而終的過程。後來發現，原來最簡單的方式，就是在某台要當成網路電台的電腦上，指定中華電信所提供的另兩個固定IP，如此就不用在擔心什麼NAT，虛擬IP的設定。（不過我現在擔心這個IP公開出來後會被攻擊？ :p）  
  
那麼現在就來簡單介紹一下，如何設定網路廣播的程序步驟。  
  
1.簡單篇：用winamp加上 shoutcast source plugin ，則winamp 即可成為網路電台聲音來源端的電台  
  
首先要下載: winapm、外掛： [Winamp DSP Plug-in ](http://www.shoutcast.com/downloads/shoutcast-dsp-1-9-0-windows.exe) 這是讓winamp播放軟體與Shoutcast Server 之間串流轉換的橋路，以及[  Shoutcast Server](http://www.shoutcast.com/download/serve.phtml)，這三個軟體。  
  
安裝好這些軟體後，首先執行shoutcast sever，然後再打開winapm下面的偏好設定（preference）,  
在 plugin的 DSP選項中，選擇「shoutcast source」，以進入設定畫面。詳細的文字說明和圖解可參考[hkfreesky精心所製作的教學](http://members.lycos.co.uk/hkfreesky/teach/)中有關於winamp plugin 的示範。  
  
![]()如果各位看到你的 Shoutcast Source main page 中，input level有出現藍色的音量表，那恭喜你，你的網路電台已經設定OK。  
  
以下圖片，就是你的shoutcast Radio 已經開通，別人要聆聽你的電台，只要在瀏覽器下輔入  
  
![]()  
  
http://yourip:8000 ，就會出現這個網面。聽眾只要點選上面紅色的「listen」，你預設的的mp3 音樂播放軟體，就可以開啟這個 pls檔案，收聽這個網路電台的節目。或是直接開啟你的播放軟體，如media player，在檔案選項下開啟位置URL，填入http://yourip:8000，即可收聽。  
  
以上就是我摸索出來Shoutcast ＋ winamp製作網路電台的教學整理。 我覺得這樣的廣播方式，是適合於預錄式的節目，一直循環地播放。至於第二種有關SAM 網路廣播軟體，則是適用於Live 式的網路廣播。我在下一節再來談談另一種SAM 的使用和設定吧。

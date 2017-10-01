---
author: jx tsai
comments: true
date: 2006-07-22 02:39:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2006/07/22/%e7%b6%b2%e8%b7%af%e9%9b%bb%e5%8f%b0%e8%a8%ad%e5%ae%9a%e4%ba%8c%ef%bc%9anicecast/
slug: '%e7%b6%b2%e8%b7%af%e9%9b%bb%e5%8f%b0%e8%a8%ad%e5%ae%9a%e4%ba%8c%ef%bc%9anicecast'
title: 網路電台設定(二)：NICECAST
wordpress_id: 612
categories:
- dotlife
- multimedia
- software
---

[上回提過](http://www.formosa319.org/a5288/?p=192)了 有關winamp plugin 和Shoutcast 的設定，基本上仍是以多數人使用的Window作業系統環境。而在我所用的OSX底下，不知有什麼方式可以來使用網路廣播操作。Shoutcast 上說明它也有適合OSX，Linux底下的支援，但是我試用了一下，它好像是透過darwin這個程式來跑，但還要自己去修改一些預設的伺服器設定，播放 器等東西，看了半天，實在不知道Shoutcast DSP Plugin怎麼在小白底下操作。  
  
查了一下MAC versiontracker  網站，多數朋友推薦的是NICECAST 這套軟體。我玩弄了一下，才找出它的Sever 也有Shoutcast 的支援，算是符合我目前網路電台伺服器使用的要求。所以在此來介紹一下Nicecast 的設定操作。  
  
打 開Nicecast 後在?windows 選項底下找出Show Sever，除了出廠預設的 Built-in Sever 之外，也可以選擇自己欲加入的其它網路電台伺服器串流，如icecast, shoutcast, live365之類的。如果你欲用自己的蘋果機做伺服器(須有一組實體IP)，則在address填入Localhost。如果是連上其它的某一台機器， 則填入它的 IP位置和密碼，port 都是8000。  
  
![]()  
完成這部份的設定後，你就可以回到Nicecast 的主畫面，按下Start Broadcast鍵，你的Shoutcast 電台即可開始運作囉。 NICECAST的音訊來源，端看你的APPLE裏所灌了哪些播放軟體，如果純粹播MP3檔案，用iTunes 即可。如果要做Mic 現場收音式的廣播，即須再搭配Audio Hijack等軟體。

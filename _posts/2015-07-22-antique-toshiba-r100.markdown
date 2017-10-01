---
author: jx tsai
comments: true
date: 2015-07-22 12:20:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2015/07/22/%e8%80%81%e7%ad%86%e9%9b%bb%e5%be%a9%e6%b4%bb%e8%a8%98/
slug: '%e8%80%81%e7%ad%86%e9%9b%bb%e5%be%a9%e6%b4%bb%e8%a8%98'
title: 老筆電復活記
wordpress_id: 130
categories:
- ordinary or complaints
- ubuntu
---

有一台十一年前買了一台東芝筆記型電腦（Toshiba Portege R100），當初就是看上它的輕薄，其配備的效能在出廠的年代中與其它機型比較起來並不算上是頂極，但居然這樣默默地陪我走過了十年以上的光陰。好啦，我承認其實這十年來，它只能算是一台「備用機」，並未被操得太過嚴重，或許這才是它能夠挺過十年的原因吧。  
  
大約一年前左右前，發現它莫名奇妙無法開機了，想說也剛好服役滿整整十年，算是「壽終正寢」，打算利用它最後一點殘餘價值送去小七回收換點零食的折價券，但一直擺放在一角未積極處理。昨天忽然福至心臨地，把它接上電源上看看是否還有反應，結果居然意外地喚醒了這台沈睡中的筆電。  
  
過去我曾經試著在其上安裝ubuntu家族的linux作業系統（較輕量級的xubuntu, lubuntu之類），但總是會遇上螢幕顯示問題，原本應是1024x768，只能呈現800x600，換句話說，就是在一片面積1280x768大小的紙片上，只有中間800x600才能看到東西，其它面積部份就成暗黑的週圍。當初因為不知道如何解決這個無法全螢幕顯示的現象，只好放棄linux 系統，改裝回原廠配給的windows xp 作業系統。  
  
在機子意外甦醒後，進入的就是久違的windows xp環境。當初購買筆電時，有搭配一組外接式的DVD ROM，一般就是用它來透過光碟作系統的重灌安裝。但因為我早已把DVD光碟機丟掉，家裏手邊也沒有其它光碟機可接，如何在其上安裝其它開機作業系統就大傷一番腦筋。雖然我已把xubuntu的鏡像檔下載下來存成USB的開機檔案，但這台老機子的bios 設定上來看，它並不支援USD FLASH 啟動開機。於是腦筋就動到這方圓十里之內可以向誰開口借DVD光碟機（方案A），或是試著透過自己家中內部網路，弄一台網路磁碟機開機的方式作安裝（方案B）。以我的個性，當是先試作方案B，因為不必閧口求人，雖然這種安裝方式我從來沒有試過。但網路上有查到其作法說明：[Toshiba R100遠程安裝](http://www.coctec.com/docs/linux/show-post-151182.html)，看來似乎不算太困難。  
  
不過我後來都沒採遠程安裝或是光碟機方式，而是利用另一個小工具取巧地安裝了xubuntu。「早年」ubuntu 為了減少世人對於安裝linux 系統過於複雜艱難的恐懼感，一度推出了在windows 作業環境下無痛安裝ubuntu 的方式： wubi(Windows-based Ubuntu Installer)，但後來因為發現了一些問題官方就不再更新支援wubi的安裝方式，還是建議使用者直接以硬碟安裝ubuntu。考慮到這台老筆電的效能，我一開始也沒打算安裝最新版本，故找到wubi 9.10版本的檔案與xubuntu 9.10鏡像檔放在同一個資料匧，就這樣居然成功地讓我在windows xp下安裝好了xbuntu。因此電腦一開機時，就會出要使用windows XP 還是xubuntu在開機選單。  
  
![toshiva r100 ubuntu](https://1.bp.blogspot.com/-AUCo8GSS2cI/V3w987qNWqI/AAAAAAAAKLI/gqGFN0rrAOUAum0NWuj1GQ2QrUk-6L8zgCLcB/s1600/grub.png)  
  
進入xubuntu之後，以前遇過的螢幕顯示縮水的情況，這次也依然如故。但我不會是遇到此問題的第一人，詢問google大神後，果然有前輩遭遇同樣的麻煩。我參考的作法是從ubuntu 論壇上的這則討論串：[can't get full screen using Ubuntu 9.10](http://forums.pcpitstop.com/index.php?/topic/175175-cant-get-full-screen-using-ubuntu-910/) 。首先確定我有安裝好了顯卡驅動程式（Trident display driver），然後照理要去修改 ／etc/X11/ 底下的「xorg.conf」這個檔案。但發現自己的系統並沒有xorg.conf這個檔案，故是硬給它新增了一個，其內容則把上述討論串第28樓朋友提供的 xorg.conf 內容給複製貼到我自己新增的檔案中。確定 etc/X11/ xorg.conf 已按此更新後，重新開機，果然登入畫面就成功變成了1024x768的全螢幕顯示。  
  
![desktop](https://3.bp.blogspot.com/-OJXprukcpe8/V3w-HuYlrpI/AAAAAAAAKLM/lZJSeLnmUIkCv5hJk6aZ2uHCB28xg9uqgCLcB/s1600/desktop.jpg)  
  
目前已把xubuntu 系統「更新」到10.04版，但還須要作許多調校畢竟隨著硬體的發展與軟體不斷昇級，這台老機子未來的作用實在不太，可能就如同之前介紹過樹莓派一樣，把它用來作為學習文字指令介面與學習編譯式程式語言的小玩具吧。

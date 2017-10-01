---
author: jx tsai
comments: true
date: 2016-01-05 08:09:00+00:00
title: CentOS 最小安裝之後:網路設定
wordpress_id: 100
categories:
- centos
- dotlife
- software
---

上回提到自己想多學習熟悉更多的Linux散佈版本，除了推薦給轉入linux新手可優先考慮Debian家族下的ubuntu/Mint外，決定再來認識另一支紅帽家族的CentOS，於是弄好了CentOS Minimal ISO 開始進行安裝。其實它的安裝過程仍是採用圖形環境介面，所以只要按指示點滑鼠並不算複雜困難。不過完成安裝程序後，開機選擇進入CentOS，卻發生了令我傻眼的結果：登入畫面居然是純文字指令環境，即使輸入 "startx", 希望可以進入圖型介面，電腦卻反應不解這道指令作用為何，這時才回過頭仔細看CentOS　Ｍinimal 的介紹，原來它只有最核心的元件，其它的軟體或組態調整都得靠使用者自己調適或下載。  
![CentOS CLI](https://4.bp.blogspot.com/-XRrnIEllnHc/V35pi7Y0FTI/AAAAAAAAKWk/bgrGBpuRiB4SXBUbeOMGWeTY5yLSqzMQACLcB/s320/centos-set-server-time.jpg)  
  
一開始我參考的是這篇：[完成 CentOS 7最小安裝要做的三十件事](https://linux.cn/article-5341-1.html)，但是卻沒耐心仔細看完它的說明，只急著在全黑的命令列打入“ifconfig”(理論上這是linux底下在命令列叫出網路卡資料的指令，一如windows下的ipconfig)，想看看電腦網路卡是否成功地啟動工作。但沒想到電腦卻傳回說它不懂這個指令，顯然最小安裝中並沒有預載其相關的軟體包，這實在讓我黔驉技窮，只好放著不管好幾個星期，不知道該如何解決這個問題。唉，無法連上網，我就無法安裝其它需要的軟體包，沒辦法安裝ifconfig 這個功能包，我就不知道如何了解目前電腦網路組態的設定狀況，這似乎是一個蛋生雞雞生蛋的困境。  
  
在這段「冷靜期」中，因某機緣，接觸到某一個網站後台新架設遠端私有雲空間的過程，懵懵懂懂地了解，原來透過SSH文字指令操作，操控遠端伺服器（CentOS作業環境）可以安裝架設網站需要的相關軟體，別人輕輕鬆鬆地把一個網站架設出來，益發刺激我自己回頭決再繼續摸索學習CentOS文字指令環境下，如何做到同樣的事。  
  
這時候我開始翻查電腦教科書，原來可以用“ip address show" 指令取代“ifconfig", 找出當前電腦中網路組態的資訊，才查出原來使用中的接線網路卡名稱是：「enp7s0」，和一般教科書上的「eth0」不同，我就是不知道這點，所以教學指南叫我要修改相關組態檔案中的網路資訊，都被亂改成為「eth0」，但我的電腦的CentOS底下根本沒有eht0這個東西，難怪設定失敗，沒法順利連網，而這也是後來才知道的錯誤。  
  
總之也不知道自己是怎麼亂改個誤打誤撞下找出上網用的有線網路卡正確代號，並指手定了內部網路中的刻意指定的虛擬IP位置後，終於順利地連上網路，不但可以成功地連網安裝其它元件，也可以讓其它電腦透過SSH作遠端操作控制，接下來就可以進入嘗試網路伺服器架設的重頭戲了。  
  
如果對於CentOs的安裝使用和基本安全設定感到不知如何入手，建議可以參考Lynda.com 教學網站上的「[Up and Running with CentOS Linux](http://www.lynda.com/CentOS-tutorials/Up-Running-CentOS-Linux/159633-2.html)」，我覺得看了教學影片示範後至少能對CentOS的環境有蠻清楚的初級認識。  
  
另外在文字指令的環境下要修改環境組態的檔案，最好要先會一兩招簡單vi/vim指令（http://www.vixual.net/blog/archives/234）。一開始我不知vim編輯器要進行模式切換，所以一打開檔案後就手忙腳亂卻又無法順利修改儲存，這大概是讓我望文字環境而卻步的一大原因吧。  
[![vim 文字編輯器 ](http://nmc.nchu.edu.tw/linux/images/vi.jpg)](http://nmc.nchu.edu.tw/linux/vi.htm)

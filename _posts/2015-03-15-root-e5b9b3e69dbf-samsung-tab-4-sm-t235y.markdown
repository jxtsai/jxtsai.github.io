---
author: jx tsai
comments: true
date: 2015-03-15 21:32:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2015/03/15/root-%e5%b9%b3%e6%9d%bf-samsung-tab-4-sm-t235y/
slug: root-%e5%b9%b3%e6%9d%bf-samsung-tab-4-sm-t235y
title: root 平板 samsung tab 4 (sm-t235y)
wordpress_id: 170
categories:
- android
- software
---

目前手上常用的這台平板電腦是老弟去年五月(2014)辦理電話續約，多付一千元所購買的入門級平板。因為他已經有了另一台ipad mini 故將這台平板讓給我。當時我還不好意思白佔便宜就用入手二年多，但還蠻上手的Nexus 7 初版與之交換，沒想到那台N7 不久就被我弟摔得稀爛。  
  
這款samsung tab 4　雖是大廠三星2014年上市的新機，但其硬體只能說是堪用的入門等級，它幾乎無法承受同時上網看視訊一邊聽音樂的運轉。其實我也不曾這樣操它，但它三天兩頭自行當機然後電池自動消耗掛掉的出捶狀況實在太多，讓我更加懷念老機子 Nexus7的刻苦耐勞。  
  
三星平板上仍然是預設了許多我看來毫無用處，卻又徒佔記憶體空間（這台機子只有8G ROM) 的應用程式，看了實在心煩，雖然很想把這些無用app移除，但這就得要先進行對機子進行root程序後，才能有權限刪除安卓系統下的應用程式。  
  
等了近九個多月終於有高上在[XDA developers 網站](http://forum.xda-developers.com/tab-4/general/sm-t235-lte-rooted-twrp-2-8-alpha1-sm-t3027059)上公布其如何讓Samsung tab 4 取得root 權限的辦法。我「大膽」地照著上面的方法操作，果然「還算順利」地完成了這台平板的root 程序。故寫下簡單的中文版的手續讓有心人可以參考一下。  
  
1). 下載原post所附的三個檔案，我進行的操作的電腦環境是在windows 7　底下，必須要用線刷。  
  
2). 在電腦上解壓檔其中 Odin3v1.85.zip，等會線刷時會用到。  
  
3). 將這個UPDATE-SuperSU-v2.46.zip 存到平板的SD卡，我是放在第一層，比較好找.  
  
4). Put TWRP_2.8.1_SM-T235_and_SM-T235Y_recovery.tar somewhere on your PC you can find it from Odin3 later.  
  
5). 平板透過USB線連上電腦後，將平板關機，然後同時長按住電源、音量鍵下方以及home bottom 約十秒鐘(就是下方中間突出的楕圓鍵，我覺得二隻手十個手指要同時按這三個鍵也不容易啊)，　就會進入一個黑色背景的警告畫面，這時可放開，然後按音量上方確認進行下一個步驟。  
  
6). 平板與電腦連接的狀況下，在電腦端開啟剛剛解壓縮的Odin3 v1.85資料夾內的執行檔，就會出現一個程式小視窗，點選右下角「PDA」，然後找出剛才下載的TWRP_2.8.1_SM-T235_and_SM-T235Y_recovery.tar，　同時option 地方原本預設有勾選的Auto-Reboot and F.Reset Time　二個選項，把它們取消後，就可以大膽地按下"start"。　  
![odin](https://3.bp.blogspot.com/-7dRpId1lf_k/V3y07pfsxCI/AAAAAAAAKOM/7QTpK4JQWEgVnBIZNmHIgpfYXzM2vJRhQCLcB/s320/odin-300x211.jpg)  
  
7). 整個過程照理不會太久，當平板完成快閃安裝後，Odin3 視窗就會出現"RESET"。  
  
8). 這時可把平板從電腦移除，接下來要進行一連串手指按來按去的操作。首先在平板上再一次同時長按住電源、音量鍵下方以及home bottom，以進入重啟畫面。  
  
9). IMPORTANT: 當平板的畫面變成全黑，趕快把原本按住音量鍵下方放掉，改按音量鍵上方，但同時其它二鍵（電源以及home bottom 仍然維持原樣不可放開）　  
  
10). IMPORTANT: 一但開機畫面出現 SAMSUNG SM-T235 LOGO ，放開電源鍵但仍同時按住立音量鍵上方以及Home bottom。  
  
11). IMPORTANT: 如果你的手指按放自如地依上述步驟操作，此刻你應可以順利地看到藍色背景的"TEAMWIN splash screen" ,意謂你已順利地進入了TWRP recovery　模式。（如下圖）如果沒有順利出現這個畫面，請再次重覆8~10的步驟。  
![](https://forum.xda-developers.com/attachment.php?attachmentid=3158709&stc=1&d=1423571848)  
  
12). 順利進入 TWRP Recovery　下， 請點選"Install"。  
  
13).　找到一開始安裝在平板SD卡上的"UPDATE-SuperSU-v2.46.zip" ，點選它進行安裝。  
  
14). 完成該檔之安裝後，從TWRP 主選單重啟（root）平板。  
  
15). 平板重新開機，如果一切順利，這時機子應該已經成功取得了root 權限。  
  
16.) 不信的話，可以下載root checker 檢查看看。  
  
root 之後，發現可以移除的軟體還是依然很有限啊XDDD (許多都說是"關鍵模組＂，深怕一但移除就出問題)

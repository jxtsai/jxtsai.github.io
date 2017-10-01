---
author: jx tsai
comments: true
date: 2015-09-28 10:18:00+00:00
title: ubuntu 常用軟體筆記
wordpress_id: 119
categories:
- software
- ubuntu
---

這兩天把原來一台已報廢（可能是顯卡壞掉）筆電的2.5吋舊硬碟（160G）拆來裝在目前算是主要工作用途的「中年筆電」上。其實原是打算買入一顆SSD固態硬碟來試試，所以拆了原機的底板看看它的硬碟安裝是否會很費功夫，結果這台Toshiba C640硬碟與記憶體的拆裝都算蠻容易的，只是第一回要扮開底版的小勾槽要用上點力（但又不能把它折彎了）。一時之間還等不到中意容量的SSD下殺特價，所以乾脆把原晾在一旁的160G舊硬碟取代原來的320G雙系統（當初劃給ubuntu的空間只有40G，雖然系統和程式目前用一用還剩15G左右應該還堪用，但心理的某種硬碟容量爽度總是不足吧），再來好好地單一安裝ubuntu，遂寫下這篇筆記，以為將來如果在其它機子上要安裝ubuntu 時，有哪些自己常用必裝軟體的清單參考。  
  
完成ubuntu 系統後，我第一步做的工作，就是把它的桌面環境改造成 [Apple Mac OX](http://self.jxtsai.info/2015/05/ubuntuos-x.html)（完全是窮酸人的心態啊）  
  
1. 安裝倉頡輸入法，現在ubunu 都直接內鍵ibus 支援注音或拼音輸入法。但沒有我較常用的倉頡（雖然常會遇上字拆不出來，得轉換注音輸入模式的肉腳）。  
2. 刪除了ubuntu 14.04 預掛中附入，但我個人不愛也用不到的軟體，例如遊戲,文字編輯器， 網路通訊軟體，BT軟體。但總體而言，ubuntu預掛中就有libre office , python 等，實在很貼心啊。  
3. 安裝GIMP/ Inkscape 或許沒有商用Creative Suite 功能強大，但對我已經大大夠用了。  
4. 安裝Sublime Text 2 ，很好用的文子編輯器，可惜無法支援中文打字，主要用它來作程式編寫用。  
5. 安裝dropbox。大量是因為雲端硬碟普及的關係，所以現在重灌系統都亳無掛念是否有資料得先另作好備分，直接大刀一砍，重新來過。  
6. 安裝 R/Rstudio，主要為目前學習資料處理用。  
7. 安裝[Revelation 密碼管理系統](http://self.jxtsai.info/2015/08/blog-post_11.html)。其實現在砍硬碟換資料，最重要的是要記得把自己存放密碼管理的資料備份一則啊。  
8. 安裝 VLC, 雖然ubuntu 裏面有其它影片觀賞軟體，但我還是喜歡這一款。  
9. 安裝 [Okular](https://okular.kde.org/)/ pdf-Shuffler, 前者是PDF文件閱讀軟體，但有劃底線重點加註記的功能。後者是簡單的 pdf 編輯器，我多半用來作文件的刪頁插頁編輯足已。  
10. 安裝字型：ubuntu 原裝套件中的中文字型只有兩三個，有時一些常見字的字體居然還會跑跳，如果要作美編，應該還是要多裝一點中文字體才好應用變化。我是參考[這篇安裝免費版的思源字體](http://ingramchen.io/blog/2014/07/ubuntu-noto-font.html)。  
11. 安裝git ,雖然自己目前還很少用到程式碼協作的版本控制軟體，但還是先裝起來好了。  
12. 安裝[python web application  hdjango](https://www.digitalocean.com/community/tutorials/how-to-install-the-django-web-framework-on-ubuntu-14-04)，同樣雖脎自己目前也還不熟django ，但是還是一併裝好吧。話說在unbutu 14.04的套裝下, python 3.4 已裝整合於其中了。當然有些數庫還是得自己安裝，像我為了學習使用python 作數據呈現，就安裝了[scipy ](http://www.scipy.org/install.html)  
13. 安裝好[LAMP Server](http://magiclen.org/lamp/) ，雖然很少在自己電腦上作網頁或架站套裝包學習，但還是先把它一次到位設定好了。  
  
目前大抵就先這樣,爽爽用。

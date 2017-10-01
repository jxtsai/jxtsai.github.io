---
author: jx tsai
comments: true
date: 2015-12-01 09:11:00+00:00
title: 電腦桌機安裝android 作業系統
wordpress_id: 108
categories:
- android
- dotlife
- software
- ubuntu
---

![word-image11](https://4.bp.blogspot.com/-0rqm8d4v0AE/V3vXBmYv9dI/AAAAAAAAKJM/1DgQKvqiTxU3dE006h1upkF2AzkBZFgdACLcB/s1600/word-image11-1024x576.jpg)  
  
近來因智慧型手機壞掉，也為了想多學習一點linux的基礎知識，開始試著在筆電上另再安裝一個android 獨立作業系統的方式。其實方法很簡單，只需要下載開發者研究釋放出來，將安卓系統移殖到三十二位元電腦系統上的[android x86](http://www.android-x86.org/) 映象檔，燒錄到USB或光碟上作成開機片或是開機USB，然後重新啟動電腦，按照一步一步的安指步驟就可以輕易地桌上型電腦或是筆記型電腦上快速安裝好安卓作業系統。唯一比較麻煩的有二件事，第一是如果欲安裝的電腦只有一顆實體硬碟的話，得事先確認這顆服役中的硬碟在作磁區分割規劃時，留有足夠的未用空間給另一套作業系統作安裝，第二件麻煩事則是如何把安卓系統選項載入到開機選單（grub2），以便有多重開機的選擇。  
  
第一個麻煩的問題，幸好因為我近來也動念想要試玩linux其它家族的版本包，所以重新切割了ALL IN ONE 電腦上320G的空間，除了200G給傻瓜系統的xubuntu外，其餘空間則平均分給了CentOS 與Fedora。不過因為在安裝過程中，發現有許多設定沒像ubuntu 那麼簡單，所以只勉強裝好了CentOS 6.7，但還不知道如何設定無線網卡，更別說是繼續安裝好Fedora。因為還未使用的硬碟磁區中又可以再分割出一小塊給　android使用。  
  
至於第二個問題，因為不會grub稍微棘手一點，雖然順利地把android安裝到電腦硬碟上，但因為安裝過程中並沒有選擇載入android 預載的grub, grbu2安裝，也就是不希望把自己原來的grub2 選單蓋過砍掉，所以如何手動做事後的開機選單設定，着實費了我一小番夫功。  
  
理論上在ubtunu 上再安裝[Grub Customizer套件](http://ubuntuhandbook.org/index.php/2014/04/install-grub-customizer-ubuntu-1404/),就可以用圖示介面比較直接的方式來編輯電腦上的開機選單。不過因為我使用的是xbuntu ，它是使用XFCE桌面環境而非GNOME，不知道是否如此，所以我即使似乎成功地安裝了grub-customizer卻無法找到它來開啟使用，所以只好硬著頭皮在無知半解的情況下試著直接去修改相關檔案的指令內容。  
  
我是參考了bethnesbitt這篇答案：[Add android-x86-4.4-RC2 to ubuntu grub](http://askubuntu.com/questions/481982/add-android-x86-4-4-rc2-to-ubuntu-grub)。特別是在　/etc/grub.d/40_custom　這個檔案下，新增了這幾行文字：  


<blockquote>menuentry "Android-x86" {  
set root='(hdX,X)'  
linux /android-4.4-RC2/kernel quiet root=/dev/ram0 androidboot.hardware=android_x86 acpi_sleep=s3_bios,s3_mode SRC=/android-4.4-RC2S <del>SDCARD=/data/sdcard.img</del>  
initrd /android-4.4-RC2/initrd.img}</blockquote>

  
注意上面的文字，要再根據你自己的狀況做修改，例如我把android 安裝在唯一硬碟的第三段磁區，所以set root='(hdX,X)'就要改成set root='(hd０,３)'，而我下載安裝的是：android-5.1-rc1，所以‘android-4.4-RC2’的部份就要改成‘android-5.1-rc1’。存檔更新後，再重新開機，不但grub 開機選單順利在最後一項出現了：Android-x86，選這個選項也終能順利進入android。  
  
![grub menu]()  
在桌機上順利安裝進入android，雖然可以順利偵測到無線網路並連線，但要從google play 下載app 卻一直卡關，開啟youtube 也無法觀看。查了一下到底問題出在哪，原來在開發者的網站上一開始就有說明：[因為未得到google 授權，無法安裝google play 軟體](http://www.android-x86.org/documents/apphowto)Ｏrz。所以只能效法[阿貴老師的作法，到f-droid](http://newtoypia.blogspot.tw/2015/01/android-x86.html)去下載原始碼公開的安裝軟體。  
  
至於在桌機或電腦上執行android作業程序的感想如何呢？嗯。。。。。螢幕畫面雖然很大，但它本質上是專為觸控螢幕設計的系統，所以在非觸控螢幕的硬體環境下，只有靠著滑鼠拖著操作，得要適應一下，有時候遇上某些軟體畫面還會自動地翻轉90度。雖然從f-droid下載了注音倉頡輸入法，但還是不知道如何切換輸入法方式。  
  
以上介紹的是在硬碟上作分區後安裝android，據說還有利用virtual box, gynemotion, android SDK等方式跑虛擬器方式在電腦上安裝使用android，會有這些利用模擬器跑android多半是技術者要軟體開發測試用途，至於真要作實質當電臘上另一款作業系統使用恐怕還是省這股力氣吧。  
![android x86]()

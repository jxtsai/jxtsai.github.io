---
author: jx tsai
comments: true
date: 2016-01-24 22:32:00+00:00
title: ubuntu 網路開機安裝法筆記
wordpress_id: 96
categories:
- ubuntu
---

[半年前提過把用了十多年的古董級筆電](http://self.jxtsai.info/2015/07/blog-post_22.html)在原作業系統windows xp下透過wubi 安裝ubuntu 家族中輕量級的桌面環境xubuntu/ lubuntu。使用下來也還算相安無事地可應付一些不太吃力的網頁瀏覧工作。不過在這台老機子上同時並存的windows xp系統（其實是被迫寄生在其下才能安裝ubuntu），總是像個卡在心頭的梗刺，很希望把它完全移除，只留下乾淨的linux作業系統就好。但因為這款老筆電並不支援usb 開機，另一種常見的光碟開機也因其附購的隨身光碟機早已被我丟棄，唯一剩下的可能性就是學習使用網路開機安裝法來灌全新的作業環境。本篇文章稍記錄分享我嚐試在PXE( Preboot Execution Environment)下選擇利用內部網路裏的另一台電腦作為服務主機，提供開機安裝軟體給老筆電啟動安裝作業程式的方法。  
  
嚐試一：主機為 windows環境，利用[tftpd32](http://tftpd32.jounin.net/)：  
結果失敗，不知為何，筆電選擇網路開機後，一直無法成功連到主機，找到啟動檔進行安裝設定。雖然按它網頁上的說明以及其它使用者的說法，看似很簡單地只要填入欲啟動安裝程式到指定的目錄，與設定IP位置，但不知為何，就是無法順利連線，只好放棄。  
  
嚐試二：主機為 windows環境，利用 serva  
找到另一篇「[Windows環境設定PXE啟動遠端電腦安裝Linux作業系統](http://www.mobile01.com/topicdetail.php?f=300&t=4195963)」，作者利用serva裝在windoows主機上，來管理控制其它電腦連線到主機上安裝作業系統，並附上以ubuntu與OPENSUSE為例的清楚圖說示範。[serva官網](http://vercot.com/~serva/)上則列出更完整列的windows以及非windows作業系統的測試成功清單與設定方法。如果是要安裝windows作業系統，只要把安裝光碟中的檔案全部複製到 C:SERVA_ROOTWIA_RIS 即可。但我試著安裝winodws xp 時，筆電卻跑出訊息回應說該版本和電腦不符之類的，讓我有點頭大。  
而透過serva 安裝非windows作業系統（泛指linux家族），則除了把欲安裝的程式檔案全部複制到C:SERVA_ROOTNWA_PXE之下外，還得編寫一個：servaasset.inf 設定檔，把它放在相應的資料夾。但這台Toshiba R100實在太過老舊，其CPU無法支援PAE(Physical Address Extension)，所以ubuntu 14, CentOS 6 以上的版本都無法安裝，透過serva 能安裝的選項有限。其中唯一試成功的，只有唯二作業系統：一是CentOS 5.11以下的網路安裝版，其一是小狗linux。然而CentOS 5的網路安裝版，目前各地備份網站中只有提供ISO鏡映壓縮檔，並無其解壓縮的檔案，而我又還不會使用在自己的內部網路建一個指定的位置讓它去抓取安裝檔案（請參考下面「鳥哥的linux 私房菜」），只好作罷。而第二個成功法，則是利用puppy linux 讓筆電可進入其系統環境中。聽說puppy linux是利用電腦記憶體來開機執行，並非安裝在電腦硬碟中。因此我試了一些方法，想在puppy linux環境下把安裝該系統安裝到硬碟裏，但一直未成。只盼日後有機會再試試，其輕巧的效能表現還蠻讓我驚豔的。  
  
嚐試三：主機為ubuntu 環境，利用tftp-server  
既然試過主機為 windows的作業環境來支援另一台電腦的網路啟動安裝之路如此的不順遂，不如回到ubuntu或是CentOS的環境下來試試，然一開始這條路徑讓我止步的原因是，找到的指南說明都偏向文字指令操作又會涉及root權限，不像windows底下好像只要搬動一些檔案即可。首先參考了[鳥哥的 Linux 私房菜](http://linux.vbird.org/linux_enterprise/0120installation.php), 相關的基礎觀念寫得還算清楚，讓我有了一點初步概念。但是實際操作上，還是不知從何下手，畢竟仍不太熟悉CENTOS的操作。再找找其它介紹ubuntu環境下的網路開機安裝法，主要參考了二篇文章：[Ubuntu 架設PXE Server](http://inpega.blogspot.tw/2015/04/ubuntupxe-server.html)；[ubuntu documentation: Installation/Netboot](https://help.ubuntu.com/community/Installation/Netboot)( On roo (the DHCP server):把這行 ”dhcp-boot=pxelinux.0,roo,172.31.0.252“， 後面的IP位置改成自己主機電腦的（無線／有線）網卡IP)。  
按照第一篇文章的操作，雖然成功地讓筆電可以指向電腦主機的IP位置，但是安裝方卻出現：無法在指定目錄找到可開機檔案的訊息。（File not Find  
PXE-M0F: Exiting Intel Boot Agent）  
此時我在/var/lib/tftpboot/ 底下放的是‘lubuntu-12.04-desktop.iso’的解壓縮檔案。只好再改試第二篇文章中的方法，下載 Ubuntu Netboot Images， 幸好在ubuntu 官方存檔的映像檔中，還存有支援non-PAE的Netboot Images。我下載了這個 netboot.tar.gz 把它解壓放到/var/lib/tftpboot/ 下。  
  
這時候再試一遍筆電重新選擇由網路啟動，竟然莫名奇妙地可以進入ubuntu的安裝設定畫面了（撒花！！）。它可是真正的netboot（也就是得連線到外部網路伺服器），所以進入安裝畫面後，還會詢問你的網路卡設定，以連線到internet去下戴某一台伺服器主機上的ubuntu安裝檔案，故真正完成整個過程，會比一般由光碟片安裝要多出點時間。  
  
![ubuntu1204](https://4.bp.blogspot.com/-O5S68t05d48/V30hUd_CLfI/AAAAAAAAKQQ/bT2UQw-t8XI5fp5-5qASz272mtxcXRVyACLcB/s1600/ubuntu1204-mini_1.png)

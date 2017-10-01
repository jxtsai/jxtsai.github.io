---
author: jx tsai
comments: true
date: 2016-08-24 05:03:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/08/24/tails-%e5%ae%89%e5%85%a8%e7%b3%bb%e7%b5%b1%e4%bd%bf%e7%94%a8%e4%bb%8b%e7%b4%b9/
slug: tails-%e5%ae%89%e5%85%a8%e7%b3%bb%e7%b5%b1%e4%bd%bf%e7%94%a8%e4%bb%8b%e7%b4%b9
title: TAILS 安全系統使用介紹
wordpress_id: 25
categories:
- infosec
- opensources
- privacy
---

2014年年底開始認真跌入linux作業環境的坑，慢慢地認識在此家族之下衍生出了不同的散佈版本。今年初偶而知道其中有一套叫作Tails開機式作業環境，其全名為：The Amnesic Incognito Live System，amnesic為失憶之意，而incognito則為匿名，故強調其保護使用者匿名與資料私密安全的功能,連世紀大吹哨者[Edward Snowden也為其背書](https://www.engadget.com/2016/01/27/edward-snowdens-os-of-choice-gets-a-major-update/)，我當時曾經試著使用安裝。雖然成功地利用第一支隨身碟開機進入了Tails作業環境，但不記得在某一個操作步驟上沒按指示亂弄而造成了原開機隨身碟的損壞（其實也不是損壞，而是原來存放TAILS原始映像檔的磁區無法把它格式化刪除），因「痛失」了一支USB隨身碟之故，我對Tails的好奇就暫時作罷。最近因為翻譯「[level-up:數位安全訓練員教材](http://self.jxtsai.info/2016/08/level-up.html)」（以及看了美劇影集Mr. Robot的電腦中的樸素桌面），其中有一大部份是介紹如何利用Tails來建構一個「安全工作環境」（safer workplace）的介紹，再次刺激了我的好奇，便利用手邊僅存「唯二」USB隨身碟再次試著安裝Tails。  
Tails的官網上其實已有針對不同的作業環境（linux, Windows, Mac OSX）各自提供了[蠻清楚的安裝指南](https://tails.boum.org/install/os/index.en.html)（尚缺中文版）。按照其上的說明，如果原電腦作業系統環境已是使用：  


  * Debian 8 (Jessie) or later
  * Ubuntu 15.10 (Wily Werewolf) or later
  * Linux Mint 18 (Sarah) or later
可直接下載Tails映像檔並透過原作業系統上的Tails installer直接利用一支隨身碟就可順利安裝。但因為我目前使用中的作業系統並不符合其開出版本條件，故仍然需要準備二支隨身碟。這其間利用一支還是二支隨身碟的差異，我想除了一方面是較舊的debian版本並無支持Tails installer 下載外，另一方面也是在「老舊」的debian版本中如何能做到核實下載的Tail映像檔沒有遭到竄改的安全顧慮吧？其實一開始，我還覺這種安全顧慮都讓我覺得有點paranoid，不過後來看到Linux Mint放在[官網上的版本被駭竄改的消息](http://www.techrepublic.com/article/why-the-linux-mint-hack-is-an-indicator-of-a-larger-problem/)，才慢慢了解許多潛伏的威脅存在並不是杞人憂天。  
  
安裝步驟  
1. 下載Tails image 映像檔，並透過DISK（linux底下的一支磁碟管理應用程式）來還原映像檔（Restore Disk Image）到第一支USB隨身碟上。過幾分鐘之後，第一支用來作為安全安裝Tails中介物的碟身碟便可順利作好了,等會要利用這支中介隨身碟來開機。  
  
2. 假設BIOS已把開機優先選項設為USB設備，故先裝第一支隨身碟插上電腦，準備利用它來開機。按理應可成功地看到Boot Tails的選項，直接選擇“live”以正常地進入到Tails作業環境。  


![](https://1.bp.blogspot.com/-HNk4tWBzzwU/V7vDJx1Y4VI/AAAAAAAAKxE/uryTNO0Q3TwcstZcfg9dhJRAnJF4cYjqQCLcB/s1600/tails_boot_menu.png)

  
3. 登入到Tails之後  
Tails的安全性是其自生系統利用電腦記憶體來開機執行，而非將作業系統掛載在硬碟上，故當電腦關機後，照理說不會留下任何使用痕跡。在首次（其實之後的每次也一樣），Tails的登入畫面會詢問你是載入哪一種語言介面，目前已有簡體中文語系。如果要使用「常存磁區」功能（稍後再介紹），則須在歡迎的登入畫面中挑選“More options”,以便先設定登入密碼。不過目前我們只是先用這支隨身碟要來製作第二支真正要使用的Tails隨身碟，故在此只要選擇“No”然後登入Tails即可。以下就是Tails樸素的桌面環境外觀。  


![](https://1.bp.blogspot.com/-RtO1GlKVb2A/V7vFwSVr6pI/AAAAAAAAKxQ/gwk3NZx8LYIFkrgWaco9qV--MNvDmWVkACLcB/s1600/desktop.png)

  
電腦接上第二支隨身碟，然後再左上方的主選單中找出Tails Installer功能（Applications ▸ Tails ▸ Tails Installer），其便會自動跳出Tails Installer的功能選項清單，在此選擇第一個“Install by cloning”，並將第二支隨身碟作為其複製對象之目標，然後電腦就自行進行Tails的復制工作了。等完成複制工作後，將電腦關機（或重新啟動），此時請把原本第一支隨身碟自電腦移除，保留第二支隨身碟利用它來開機啟動Tails。理論上這樣就完成Tails開機隨身碟的製作，可以安心地使用它來進行匿名通訊或私密資料處理的工作。Tails本身映像檔約為1.2G，需求的USB容量最少也要有4G空間，正常安裝後大約佔用了1.5G左右的容量，而這1.5G可包含了掛載一些方便的自由軟體工具，例如辦公室軟體Libre Office套件、向量性圖檔編輯軟體inkscape，匿名的安全上網瀏覧器TOR，還有可用來清理檔案元數據資訊的MAT(Metadata Anonymisation Toolkit)軟體，作為應急或特殊戕況下使用的作業系統與工具包，應該說是縒縒有餘了。  
  
4. Tails Persistence Disk  
Tails這種利用USB隨身碟，把運行與活動記錄暫存在電腦記憶體的處理方式，雖然盡可能地做到了來無影去無踪的數位私密安全使用實踐，但某些敏感私密的檔案、資料或文件勢必得另外存在其它地方（e.g. 另一支隨身碟或原安在電腦上的硬碟磁區），這又有點麻煩，故Tails還提供了一種“persistent storage”功能。它是在原本的USB隨身碟上另外切割建立一個加密磁區以便讓使用者可以存放敏感私密的檔案、文件或PGP密鑰等資料。若想要在USB隨身碟建立這個功能，則在一開始Tails的歡迎登入畫面中挑選“More options”，即會出現引導使用者設定登入密碼。而設定persistent storage則是在“ Applications ▸ Tails ▸ Configure persistent volume.”進行。照理說，若將此隨身碟安插到其它的非Tails的linux作業環境下，也能看到這個加密磁區被掛載讀到，不過Tails安全設計上是建議越少使用常存磁區越好，故若在其它作業系統上雖然可能可以開啟或編輯其上的檔案，但似乎得先花上一點破解功夫。例如最下面二圖中，我試著在ubuntu底下要讀取persistent volume內容，雖然輸入了該磁區的開啟密語，但仍然傳回錯誤訊息，無法讀取其內容。  
  
![](https://2.bp.blogspot.com/-nwFnIaG6bAY/V7xjK_rZAdI/AAAAAAAAKxg/1RhmbYPIMds2SSlwUawiTsEYUWEmHVRpQCLcB/s1600/persistance.png)  
  
![](https://3.bp.blogspot.com/-SQuB2kzuljo/V70n6CfgmNI/AAAAAAAAKx0/7bHYK3wLzNMGZsuH5_rrFLrwOV3Zyi80gCLcB/s1600/pass.png)  
![](https://3.bp.blogspot.com/-1TCcPUXifno/V70oDEXtqLI/AAAAAAAAKx4/ciU0HkVL-zQeyoFOk6AbuFPg0crqk8WigCLcB/s1600/error.png)  
  
其它參考資源：[  
自由亞洲電台翻墙问答：如何启动“手指” 安装Tails？（视频）](http://www.rfa.org/cantonese/firewall_features/firewall-tails3-05132016075748.html)

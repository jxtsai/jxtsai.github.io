---
author: jx tsai
comments: true
date: 2016-05-20 09:48:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/05/20/tor%e7%80%8f%e8%a6%a7%e5%99%a8%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97/
slug: tor%e7%80%8f%e8%a6%a7%e5%99%a8%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97
title: TOR瀏覧器工具指南
wordpress_id: 74
categories:
- human rights
- localization
- opensources
- Security First
- umbrella app
---

繼續還是Security First: umbreall app 工具中文化資料初稿，這回介紹的是「當紅」的網頁匿名瀏覧器。之所以私心覺得它正當紅，而且會越來越好，恐怕有一大因素是在電子前哨基金會（EFF）服務了22年的前執行長Shari Steele去年年底加入了其專案團隊,成為TOR專案的領導推動者。Shari　顯然不是什麼技術型的駭咖，其背景出身為法學院訓練出來的訴訟律師，而其十多年長期在EFF的經營風格就不是什麼突顯個人風頭而是致力於議題與組織整體的能見度提升，也讓ＥＦＦ從一個小型的ＮＧＯ，能在成立２５年後成為數位時代中權利倡議且佔有受人尊敬言權的中型ＮＧＯ，這點令我很是默默地尊敬啊。  
第一次使用TOR是約在2010年左右，當時的使用者體驗是：「靠，好麻煩好難用啊」。去年再重新下載使用，其用戶體驗的確已大幅提升。建議如果要訪問某一些不想讓別人知道的網站也不想讓他人知道在網站上進行何種行為，請採用TOR瀏覧器  
  
***本文為Security First製作的手機應用umbrella app正體中文化翻譯系列資料之一。目前仍為初稿狀態，虛心接受指正批評。原始的json資料格式配合app電子書的html編輯標籤，轉貼到部落格上排版混亂也欠缺原始圖檔請見諒。***  
  
WINDOWS系統下的TOR工具指南線上匿名與對抗網路審查利器  
![tor browser](https://3.bp.blogspot.com/-0o-kt6fLjwI/V34s2X2O_XI/AAAAAAAAKUo/86d9DKbcBOozKOw4tad0uDL7FOOYwItQgCLcB/s1600/tor.png)   
**學習內容: [網際網路](umbrella://lesson/the-internet)**  
**本指南將簡介如何使用[Tor瀏覧器軟體包](https://www.torproject.org/projects/torbrowser.html.en) 於Windows作業系統上.  
**電腦系統需求:** 網路連線,運行於Windows環境的電腦  
**本指南使用版本:** Windows: Windows 7 Ultimate; Tor Browser Bundle: 3.6.2  
**版權宣告:** 免費自由軟體; 混合式自由軟體  
**程度:** 中級  
**其它參考資料:** [https://tor.stackexchange.com/](https://tor.stackexchange.com/)  
所需時間:** 15-30 分鐘  
**使用Tor可讓你 :**瀏覧網路躲避審查;匿名地瀏網  
  
**1.0 開始之前**  
Tor 是由志工所維護的一個網路服務，它透過遮蔽來源與身份技術提供了隱私保障與線上匿名功能 .它也能保護你和Tor 本身網路保持距離.當使用網址時有些人可能需要視情況進行匿名或保護隱私, Tor 瀏覧器即提供了一個快速而容易的方法來使用其網路.最簡單使用TOR的方法就是利用它的軟體包,  其包含了網頁瀏覧器、Tor 軟體以及其它相關的有用工具可讓你更安全地近用網站資訊.  
Tor 瀏覧器一如其它的網頁瀏覧器一樣，除了它會讓你的連線通訊要透過Tor, 這會讓監控者難以知道你在網路中的行為,也讓他人難以知道你的來源以及造訪了哪些網站.但是要記得，只有透過 Tor 瀏覧器進行的網頁活動才會被匿名.在電腦中安裝了Tor 瀏覧器並不會影響電腦中其它使用的軟體也變得匿名  (例如其它的一般網頁瀏覧器).  
  
**2.0 取得Tor 瀏覧器軟體包**  
開啟原用的網頁瀏覧器，如Mozilla Firefox 或Internet Explorer，然後在網址處輸入: [https://www.torproject.org/projects/torbrowser.html.en](https://www.torproject.org/projects/torbrowser.html.en) . 如果你是透過搜尋引擊 來找Tor 瀏覧器軟體包，請確認它的網址是正確的.![](http://self.jxtsai.info/tool_torwin1.png)點擊紫色的下載按鍵來下載程式安裝包.![](http://self.jxtsai.info/tool_torwin2.png)  
網站會自動偵測你的作業系統，因此用WINDOWS戶將可以得到所合適的檔案. 如果你想要不同的程式安裝版本,你可以滑動到下方的Tor 瀏覧器下載區來找到你需要的檔案.![](http://self.jxtsai.info/tool_torwin3.png)  
許多瀏覧器會詢問確認你是否要下載該檔案，例如 Internet Explorer 11 會在視窗下方顯示出一個橙色的警示列.![](http://self.jxtsai.info/tool_torwin4.png)一般最好是先把檔案存在電腦上再進行安裝. 所以先點擊儲存鍵. 這個示範中顯示了Tor 3.6.2版本的安裝包, 這是本指南撰寫時所介紹的安裝版本. 或許你在讀本手冊時，已有了其它更新的版本.  
  
**2.1 安裝Tor 瀏覧器軟體包**  
下載完成後, 你可以到檔案暫存的位置來開啟資料夾.通常暫存的位置是在「下載」 “Downloads”目錄裏.滑鼠雙擊程式安裝檔案 _torbrowser-install-3.6.2_en-US.exe_![](http://self.jxtsai.info/tool_torwin5.png)此時會出視一個關於軟體來源的警告視窗 .你必須小心注意這些警告以確認是否為你要安裝的軟體、來自可信任的官方網址、透過安全的連線方式而取得. 如果一切都沒問題,那麼就繼續往下走，點擊執行鍵.![](http://self.jxtsai.info/tool_torwin6.png)有一個小視窗會詢問你要使用什麼語言包 ，它提供了多種選項，選擇你要的語言後點擊“OK”鍵.![](http://self.jxtsai.info/tool_torwin7.png)這時候會出現一個新的小視窗告訴你Tor 瀏覧器將要被安裝的位置. 一般預設的位置是你的電腦桌面，當然你可以依習慣來改變你想要安裝的位置, 不過現在我們先讓它維持預設的狀態.![](http://self.jxtsai.info/tool_torwin8.png)  
當安裝完成後，你可以看到一個視窗告之安裝程序已完成. 如果你點擊完成鍵,  Tor 瀏覧器會自動立即開啟. 現在先取消執行Tor 瀏覧器的選項，我們稍後再回來使用它.如果你不小心點擊了檢查項而Tor 瀏覧器開始啟動了，只要先把它的視窗關上即可。![](http://self.jxtsai.info/tool_torwin9.png)Tor 瀏覧器軟體包並未一併安裝其它程式，也不會出現在你電腦上開始的程式選單中.![](http://self.jxtsai.info/tool_torwin10.png)  
  
**3.0 使用Tor 瀏覧器軟體包 **  
**第一次使用Tor 瀏覧器**:當你完成程式安裝時，並未選擇立即啟動,這是第一次啟動Tor 瀏覧器. 如果你完全按照預設的安裝設定，你將會在電腦桌面上看到一個名為「Tor 瀏覧器」“Tor Browser”的資料夾.![](http://self.jxtsai.info/tool_torwin11.png)打開這個資料然後雙擊其中一個叫作“Start Tor Browser”的檔案.![](http://self.jxtsai.info/tool_torwin12.png)第一次啟動Tor 瀏覧器, 你會看到一個視窗可讓你調整必要的更動. 當然也可以之後再回來進行變動,所以先來連上 Tor網路，請點擊「連線」“Connect”.![](http://self.jxtsai.info/tool_torwin13.png)點擊連線後,會出現一個綠色列桿的新視窗顯示Tor 瀏覧器正在啟動中.![](http://self.jxtsai.info/tool_torwin14.png)通常第一次啟動會花較長的時間，請保持耐心,過幾分鐘後， Tor BrowserTor 瀏覧器就完成連線設定而會開啟網頁瀏覧器，恭喜你成功安裝好Tor 瀏覧器.![](http://self.jxtsai.info/tool_torwin14.png)  
  
**Mac 系統下的TOR工具指南 **  
**學習內容: [網際網路](umbrella://lesson/the-internet)**  
**本指南將簡介如何在Mac電腦上使用[Tor瀏覧器軟體包](https://www.torproject.org/projects/torbrowser.html.en).**  
**電腦系統需求:** 網路連線,運行於Mac OSX環境的電腦  
**本指南使用版本:** Tor Browser Bundle: 3.6.2  
**版權宣告:** 免費自由軟體; 混合式自由軟體  
**程度:** 中級**  
其它參考資料:** [https://tor.stackexchange.com/](https://tor.stackexchange.com/)  
所需時間:** 15-30 分鐘  
**使用Tor可讓你 :**:瀏覧網路躲避審查;匿名地瀏網  
  
**1.0 開始之前**  
Tor是由志工所維護的一個網路服務，它透過遮蔽來源與身份技術提供了隱私保障與線上匿名功能 .它也能保護你和Tor  本身網路保持距離.當使用網址時有些人可能需要視情況進行匿名或保護隱私, Tor瀏覧器即提供了一個快速而容易的方法來使用其網路.最簡單使用TOR的方法就是利用它的軟體包,其包含了網頁瀏覧器、Tor 軟體以及其它相關的有用工具可讓你更安全地近用網站資訊.**Tor瀏覧器一如其它的網頁瀏覧器一樣，除了它會讓你的連線通訊要透過Tor,這會讓監控者難以知道你在網路中的行為,也讓他人難以知道你的來源以及造訪了哪些網站.但是要記得，只有透過 Tor瀏覧器進行的網頁活動才會被匿名.在電腦中安裝了Tor 瀏覧器並不會影響電腦中其它使用的軟體也變得匿名  (例如其它的一般網頁瀏覧器).**  
  
**2.0 取得Tor 瀏覧器軟體包**  
開啟原用的網頁瀏覧器，如Mozilla Firefox 或Internet Explorer，然後在網址處輸入: [https://www.torproject.org/projects/torbrowser.html.en](https://www.torproject.org/projects/torbrowser.html.en). 如果你是透過搜尋引擊來找Tor瀏覧器軟體包，請確認它的網址是正確的.![](http://self.jxtsai.info/tool_torosx1.png)點擊紫色的下載按鍵來下載程式安裝包.![](http://self.jxtsai.info/tool_torosx2.png)  
網站會自動偵測你的作業系統，因此用WINDOWS戶將可以得到所合適的檔案. 如果你想要不同的程式安裝版本,你可以滑動到下方的Tor 瀏覧器下載區來找到你需要的檔案![](http://self.jxtsai.info/tool_torosx3.png)許多瀏覧器會詢問確認你是否要下載該檔案.  
一般最好是先把檔案存在電腦上再進行安裝.所以先點擊儲存鍵  
  
**2.1安裝Tor 瀏覧器軟體包 **  
下載完成後, 你可以到檔案暫存的位置來開啟資料夾.通常暫存的位置是在「下載」 “Downloads”目錄裏.滑鼠雙擊程式安裝檔案.雙擊所下載的程式安裝檔案，它會自動開啟 .dmg 格式檔.(近期版本的OS X, 你可能會被警告此軟體來自一個未經辨別的開發者"unidentified developer" ，你可以點選滑鼠和“control”來選擇 "open"以避開這些警告訊息).把這些檔案拖曳到應用程式集下， Tor 瀏覧器應用程式將會出現，你也可以把它釘在下方的工具列中.![](http://self.jxtsai.info/tool_torosx4.png)  
**第一次使用Tor 瀏覧器**:從應用程式集來打開Tor 瀏覧器目錄，然後雙擊一個檔名為“Tor Browser”的檔案.第一次啟動Tor 瀏覧器, 你會看到一個視窗可讓你調整必要的更動. 當然也可以之後再回來進行變動,所以先來連上 Tor網路，請點擊「連線」“Connect”.點擊連線後,會出現一個綠色列桿的新視窗顯示Tor 瀏覧器正在啟動中.![](http://self.jxtsai.info/tool_torosx5.png)通常第一次啟動會花較長的時間，請保持耐心,過幾分鐘後， Tor 瀏覧器就完成連線設定而會開啟網頁瀏覧器，恭喜你成功安裝好Tor 瀏覧器.  
![](http://self.jxtsai.info/tool_torosx6.png)

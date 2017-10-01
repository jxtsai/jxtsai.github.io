---
author: jx tsai
comments: true
date: 2016-05-23 10:31:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/05/23/psiphon-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97/
slug: psiphon-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97
title: PSIPHON 工具指南
wordpress_id: 72
categories:
- android
- localization
- opensources
- Security First
- umbrella app
---

本身沒用過而且最近翻的心煩意燥，沒什麼好說的。  
  
***本文為Security First製作的手機應用umbrella app正體中文化翻譯系列資料之一。目前仍為初稿狀態，虛心接受指正批評。原始的json資料格式配合app電子書的html編輯標籤，轉貼到部落格上排版混亂也欠缺原始圖檔請見諒。***  
  
**Psiphon 工具指南-**--審查對付   
![psiphon](https://3.bp.blogspot.com/-Tc4xF-mrV8g/V34qj8j0_wI/AAAAAAAAKUU/UTAfzqes5LYWqpwdBJ8svjzEXsLMmm4NgCLcB/s1600/psiphon-1-1024x576.png)  
**學習內容:[網際網路](umbrella://lesson/the-internet)**  
**下載處:** [https://psiphon.ca/en/download.html](https://psiphon.ca/en/download.html)  
**系統需求:** 網路連線, 運行 Windows系統的電腦或是Android 2.2 版本以上的手機( 給 iPhones 和 Mac OS X的 Psiphon 3版即將發佈)  
**本指南所用版本:** Psiphon 3  
**版權宣告:** Free open-source software; GNU GPL Version 3  
**程度:** 初學者**  
其它參考資料:** [https://psiphon.ca/en/user-guide.html](https://psiphon.ca/en/user-guide.html)  
**所費時間:** 5 分鐘  
**Psiphon 可讓你:**透過電腦和手機安全地近用網際網路上被封鎖的網站與應用程式。  
  
**1 開始之前**  
**提醒:**  Psiphon 團隊發現了一個特定的惡意軟體出現在Psiphon 3 Windows 的執行環境下.這個惡意軟體以zip壓縮檔形式散播名之為 "pisphone3.zip"出現在 www.copy.com 以及其它地方. 這個壓縮檔中包含了惡意的執行檔 "pisphone3.exe",其具有 [Virus Total](https://www.virustotal.com/en/file/54201e181615c7eb18ee5a5ca3a0b7924cf3097ac5214fbee530741b6a6bc3da/analysis/1372262585/)所描述的特性。注意到其檔名為錯誤的拼法. 這個 Windows可執行檔並無 Psiphon Inc.的數位簽章。在未檢查其數位簽章前，不要任意地執行下載的 Psiphon檔案,也請參考[這裏](https://psiphon.ca/en.html#is_my_psiphon_3_for_windows_authentic)的說明。  
另外要注意的是：雖然Psiphon 並不會讓個別使用者的IP位置與任何一處造訪的網址發生關聯 , 但它本身是主要為了用於對付網路審查的躲避工具，而無法保證能隱匿用戶身份。  
  
**2 在安卓手機上使用Psiphon**  
到[此處下載](https://psiphon.ca/en/download.html)合適的版本。   
從手機上的郵件連結網址或是透過瀏覧器下載其APK檔案後開始安裝.(如果遇上錯誤訊息,你可能需要 [開啟「網頁載入」(siteloading)功能](https://psiphon.ca/en/faq.html#android-enable-sideloading)  
當啟動 Psiphon 應用程式,它會自動地連結到 Psiphon 網路.當你看到左上角Psiphon 旁邊的＂P＂出現，就表示Psiphon正透過 VPN連線 或是整個設備模式中所有的應用程式皆經由 Psiphon通道而對外連線.在狀態分頁下, 你可看到螢幕中間有一個＂ P＂出現。這個＂P＂字的顏色顯示了 Psiphon的連線狀態.灰色: 連線中;紅色: 無連線;藍色: 已連線![](http://self.jxtsai.info/tool_psiphon1.png)  
若要將Psiphon通道運行在 _全機Whole Device_ 模式, 你的手機必須運行Android 4.0以上版本或是取得rooted最高權限 . 否則該功能無法運行.一旦應用程式已連上網路, 它會自動開啟Psiphon 內鍵的瀏覧器.而手機版的 Psiphon 則無法自動將手機上其它程式的網路連線預設通過其對外連線 ,唯中有Psiphon內鍵的瀏覧器會通過Psiphon網路運行。![](http://self.jxtsai.info/tool_psiphon2.png)  
當開啟 Psiphon 瀏覧器時:左上角出現的＂P＂顯示表示了Psiphon 正在運行,而在畫面中間偏左的箭頭圖示則是讓你能夠變換分頁;下方的＂X＂鍵則是關閉目前分頁;同樣也是頁面下方的星星則是可將目前所在頁面存到書籤中＂+＂ 則是開啟另一個新分頁  
  
**3 Psiphon for Windows**  
[此處下載](https://psiphon.ca/en/download.html)合適的版本後, 執行該程式.(記得要先 [確認所下載的Psiphon是經過認證授權](https://psiphon.ca/en/faq.html#authentic-windows).)  
當執行時,它會自動彈出一個安全警示視窗顯示該程式是由Psiphon Inc.的合法產品![](http://self.jxtsai.info/tool_psiphon3.png)  
當你執行Psiphon後它會自動連上網路、當其試著連線時會出現一個旋轉的小圖示.你可以選擇以下任一個通道模式: **VPN, SSH, or SSH+ **  
一般我們建議選擇 **VPN** 選項,它意謂此刻電腦上所有網路流量都是通過 Psiphon通道管理.SSH/SSH+與VPB之間主要的不同處在於SSH是一種特定的應用，而VPN 則可以加密你電腦上所有流量資訊. 當開啟VPN後，你所有的流量都會被加密，如網頁的瀏覧、網路電話Skype和電子郵件等都會躲避網路審查.在 Psiphon的 SSH 和 SSH+模式下,則會自動設定代理而讓應用程式的流量會遵守Psiphon所設定的通道. 這是主要大型網頁瀏覧器遵照的預先設定. SSH＋ 迷亂方式是在SSH最上層再加上一道亂數層級以避免協議的指紋收集。  
在SSH and SSH+ 模式下, Psiphon 提供了分開的選項可讓國外流量經行代理通道而國內的流量則不必.檢查不使用代理器選項來開啟分開通道功能. 當這個選項運作後,未代理的域名會在訊息區內被通報。  
如果你要快速連上國內網站且你的威脅模式許可，可以選擇SSH/SSH+ 方式. 但我們還是建議最好**使用VPN**.  
連上 Psiphon伺服器後，可看到綠色標點圖示出現在視窗的左方![](http://self.jxtsai.info/tool_psiphon4.png)  
當關閉程式後, Psiphon會自動斷線。也可以再點擊圖示重新連線.記住:由於 Psiphon 3 是以 VPN為基礎, 它可以代理你所有的網路連線流量,不僅只是網頁流量而已  
你的電腦與VPN伺服器之間的交通流量是受到加密的,但是在沒有 HTTPS 的網站與伺服器之間並未加密。(這同樣適用在其它網路服務上，例如當使用Outlook or Thunderbird連到未加密 non-SSL 的電郵服務商伺服器，其當然也未能加密.).當你未建立連線時, 你就不是使用VPN。電腦上雖然安裝了 Psiphon 3 但不表示你必須都得透過代理對外連線.使用VPN，網頁的載入可能會比較慢，這是正常現象因為瀏覧器並非直接指向目的網址。有些收費的VPN服務可能會比免費的Psiphon 3連線快速, 但你最好先仔細了解這些服務商是否值得信任交付你的資訊,尤其有些公司會把你的資料與其它單位分享或是出售。

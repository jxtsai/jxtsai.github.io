---
author: jx tsai
comments: true
date: 2016-05-10 16:37:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/05/10/adium-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97/
slug: adium-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97
title: ADIUM 工具指南
wordpress_id: 82
categories:
- human rights
- localization
- opensources
- Security First
- umbrella app
---

近期會在部落格上貼出進行中的手機應用umbrella app 的正體中文化初稿內容。（有一種沒稿可用，所以拿譯文來充當了事的敷衍感啊XD）  
  
![umbrella app, security first](https://4.bp.blogspot.com/-_0IZTbtydrU/V35IZVC1ziI/AAAAAAAAKV4/FkSc1jv03rAekKWFG0GdFIn8oBS2JitfACLcB/s320/security-first.jpeg)  
  
稍微介紹一下umbrella app 這套工具，它是由一家名為「[Security First」](https://secfirst.org/index.html)所制作推廣的一套給人權工作者、新聞記者、人道援助者等可以直接下載在手機上方便查看一些簡單的電腦數位資訊安全知識以及實際受到人身威脅如何尋求協助的電子工具書。因為本質上更接近電子書或行動版的網站，而不是程式碼與字串，所以多語化的翻譯工作就是得處理許多前後有內文脈絡與字句段落意義的內容而非只是字串對應的翻譯。我希望能上半年把中文化的初稿完成，為了鞭策自己（？）也為了多介紹這套工具（部份）的確對華文讀者有實用意義的知識，所以就把一些材料放到自己的部落格上。目前第一系列會同步放出來的是有關數位通訊上最佳安全工具的介紹，至於其它有關現實中人權工作者會遇上的壓力症候或是遇上被綁票拘禁的求生指南，目前還沒譯不知內容是否有必要放過來。  
在完成正體中文化的初步翻譯，希望可以自己來試試把[umbrella app 原始檔案程式碼](https://github.com/securityfirst)加入翻好的中文包來試用與改正中文內容。若有網友有興趣一起加入中文化的工具，也歡迎到[Transifex網站](https://www.transifex.com/otf/umbrella-app/)來幫忙。  
  
***本文為Security First製作的手機應用umbrella app正體中文化翻譯系列資料之一。目前仍為初稿狀態，虛心接受指正批評。原始的json資料格式配合app電子書的html編輯標籤，轉貼到部落格上排版混亂也欠缺原始圖檔請見諒。***  
  
**Adium & OTR**：Mac電腦上的安全的即時通訊軟體  
學習內容: [傳送訊息](umbrella://lesson/sending-a-message)  
下載網址:[https://adium.im/](https://adium.im/)  
系統要求 (Adium 1.5 以上版本): Mac OS X 10.6.8 或更新, 蘋果麥金塔電腦.  
本指南中所使用的版本: Adium 1.5.9  
版權聲明:GNU GPL  
其它參考資料:[https://pressfreedomfoundation.org/encryption-works](https://pressfreedomfoundation.org/encryption-works);[https://adium.im/help/](https://adium.im/help/)  
程度:初學者-中級  
所費時間:15-20 分鐘  
![adium](https://2.bp.blogspot.com/-vRUdIb1zsug/V35Ir4__2iI/AAAAAAAAKWA/LltiXNJG4pEEV8VCNvUWQ1ix0K4fy35wgCLcB/s1600/MultiProtocoleAdium.jpeg)  
  
Adium是運行於蘋果電腦上一套免費開源的即時通訊軟體，它可讓你和使用不同聊天協議的朋友進行多方對話，包括  Google Hangouts, Yahoo! Messenger, Facebook chat, Windows Live Messenger, AIM, ICQ,  XMPP等等.  
OTR (Off-the-record) 則是一個讓人們可以運用其熟悉工具進行私密通話的協議. 不要與Google的“Off the record” 搞混了，後者只是取消了聊天記錄的功能但並未加密或認證其能力.對Mac使用者而言, OTR 會內建在Adium軟體客戶端.  
OTR 可以執行行端與端之間的加密.這表示你可以使用它來與其它聊天服務如Google Hangouts或 Facebook來進行加密通話而這些公司無法取得對話的內容. 這與Google and AOL 使用”off the record“字眼的服務協議不同，後者只是指其對話不會被記錄但並未加密.  
  
**為何該使用Adium + OTR?**  
當你使用Google Hangouts 或 Facebook chat 等通訊軟體時，雖然在它們的網站上有使HTTPS安全層級 ,這表示你傳送出的聊天內容免於被駭客或第三方人士知道. 然而這不表示Google或 Facebook就會妥善保護你的通訊,他們仍可以看到你的聊天內容也可能把它們交給政府當局.  
下載安裝Adium之後,可以使用多重帳號同時登入 . 你可以同步使用Google Hangouts, Facebook, 或 XMPP. Adium讓你也可不用OTR來進行聊天，因為只有在雙方電腦上都安裝啟用OTR時，它才能發揮功效.  
Adium 可以進行類外認證以確保你聊天的對象是你所認為的人而不是遇上了中間人攻擊(MITM attack). 每一次的聊天對話,都有一個功能選項可以顯示你和通話聊天者的密鑰指紋碼. "密鑰指紋碼"是一串字元像是"342e 2309 bd20 0912 ff10 6c63 2192 1928",它用來認證公鑰.透過其它溝通方式（如twitter直接簡訊或email）來交換彼此的指紋碼,以確保沒其它人介入你們的對話中.  
  
**限制:何種情況下我不應使用Adium + OTR?**  
科技人員有一種用語來描述當一個程式或軟體技術可能有弱點或易受外部攻擊:他們稱之為有大的攻擊表面(large attack surface) Adium 就有這樣的問題. 它是一個複雜的程式,而安全性並不是放在其優先考量. 它也有一些程式臭蟲,某些地方可能被政府或大公司用來入侵使用者的電腦. 使用Adium來加密你的通訊內容可以好好地防護非針對式網路聊天大規模監控,但如果你認為自己很可能成為資源充沛攻擊者（如國家機器）所針對攻擊的對象，你就該考慮強度更高的預防手段,像是PGP 加密電子郵件.  
  
**在你的Mac電腦安裝Adium + OTR**  
第1步: 安裝程式  
首先,在你瀏覧器上打開[https://adium.im/](https://adium.im/) 網址. 選擇下載 Adium 1.5.9.下載的檔案格式為末檔名.dmg 或是磁碟映像檔, 將之存於某一個資料夾下（大多為downloads folder）.  
雙擊已下載的檔案，將會自動跳出視窗如下:![](http://self.jxtsai.info/tool_adium1.png)將Adium 圖示移到應用程式資料夾下進行安裝.一但安裝完畢在你的應用程式夾下找到它並雙擊來開啟.  
第2步: 設置帳號(s)  
首先, 你要決定使用哪一種聊天工具或是通訊協議.這個設定過程都有幾分類似但不同的工具並不完全相同. 你需要知道每一種工具或通訊協議的用戶名稱以及你的密碼.  
到Adium 上方的選單中，打開偏好設定就可以進行帳號設定，它會自動開啟另一個小視窗.在其中選擇「Account」然後點擊下方的"+"符號.你會看到如下的畫面:![](http://self.jxtsai.info/tool_adium2.png)  
選擇你要登入的程式. 從這裏你會被問到要求輸入帳號與密碼,或是使用Adium's授權工具來登入. 小心地依照 Adium's指示.  
  
**如何啟動OTR Chat**  
一旦登入帳號後, 你就可以開始使用OTR.  
記住:為了正確使用OTR通話,雙方的聊天程式都必須支援OTR.  
第1步: 啟動OTR chat  
首先,確認對方有使用OTR,然後開始與他們透過Adium 聊天. 開啟聊天視窗後，你會在左上方看到一個小小鎖鑰圖示的. 點擊這個鎖然後選擇"Initiate Encrypted OTR Chat."  
第2步:確認你的連線  
你開始通話時對方接受了邀請，你就會看到這個小鎖圖示關閉; 這樣你就知道目前的聊天內容有受到加密(太棒啦!) 咦等一下, 還有一個步驟要進行!  
此時,你已啟動了一個尚未認證但有加密的聊天. 這表示雖然你的聊天對話是加密的,但不保證你所聊天的對方是否真是你要找的人. 除非你們處在同一個空間裏可以看到彼此以及電腦畫面, 確認對方的身份可是重要的一步. (更多的資訊請參考EFF電子前哨基金會的[重要的認證查證](https://ssd.eff.org/en/module/key-verification#overlay=en/node/37/).)  
要確認另一名Adium使用者的身份, 再次點擊視窗上的小鎖鑰圖示,然後選擇"Verify"，你可以看到有一個視窗會顯示出你和對方的指紋碼. 有些 Adium版本只支援手動式的指紋碼認證，所以你和聊天對象得需要用某些方式彼此確認Adiums顯示的指紋碼是否相符.  
最簡單的方法是向對方大聲念出指紋碼內容來確認，但這方法不一定能做到.完成這個任務也會依彼此的信任程度而有不同方式. For example, 例如你可以透過電話向對方念出你的指紋碼如果你可以認出對方的聲音或是透過PGP認證的通訊方式. 有些人會把自已的公鑰公佈在自己的網站, Twitter 帳號或是名片上.  
最重要的是讓你可以查證每一個字母與數字都彼此符合.  
現在你總算可以好好地進行加密聊天與確定通話對象身份了。什麼? 還有一件事要做！ Adium會主動記錄你的 OTR-encrypted 聊天並將之儲存在你的電腦硬碟上. 這意謂著即使聊天內容受到加密保護，但卻也以原始文字方式被存在你的硬碟.要取消記錄功能, 點擊Adium上方的選單下的「偏好設定」.在新視窗下選擇「一般」然後取消上面的"Log messages" 與"Log OTR-secured chats." 你的設定應該如下圖所示![](http://self.jxtsai.info/tool_adium3.png)  
當 Adium 顯示新訊息的通知時, 這些訊息內容很可能也被OS X 通知中心所記錄. 這樣儘管Adium 不會在電腦上留有你的通訊追查痕跡,但你或對方的Mac電腦OS X版本或許會保留下記錄. 要阻止這個,你可能要取消通知功能.在偏好設定的視窗下選擇「事件」，然後尋找任何表示「顯示通知」的條目.每一筆資料,透過點擊灰色三角符號來開啟，然後點擊最近新曝露的一行其上有 "Display a notification," 然後點擊下方的"-"圖示來移除該行. 如果你擔心留在電腦上的記錄, 你該該啟用全磁區加密功能，它可以幫助你保護資料防止沒有密碼的第三方取得電腦可打開內容.![](http://self.jxtsai.info/tool_adium4.png)

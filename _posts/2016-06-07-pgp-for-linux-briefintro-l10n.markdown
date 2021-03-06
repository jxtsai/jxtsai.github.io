---
author: jx tsai
comments: true
date: 2016-06-07 09:33:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/06/07/pgp-for-linux-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97-2/
slug: pgp-for-linux-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97-2
title: PGP for Linux 工具指南
wordpress_id: 68
categories:
- localization
- opensources
- privacy
- Security First
- umbrella app
---

本文應該是[Security First's umbrella app](https://secfirst.org/index.html) 一系列中文正體化工作草稿的倒數第二篇。剩下的幾則未進行中譯的字串，就留待其它小伙伴們加入協助了。今天貼出的是介紹如何進行電子郵件數位通信加密的工具ＰＧＰ，另外還有一篇將會是介紹在android手機版本的ＰＧＰ電郵加密工具ＡＰＧ與Ｋ９。  
  
去年開始了解電子郵件加密以來，依樣[畫箶廬地製造了一把ＰＧＰ密鑰](http://self.jxtsai.info/2015/09/gpg.html)，但當然到目前為止一點都派不上用場ＸＤ。幾年前也有人開發出了網頁電郵版的ＧＰＧ加密外掛[Mailvelope](https://www.mailvelope.com/),這個專案的語言包目前也被Open Technology Fund放到了transifex 上進行多語化的工作。其台灣方面的ＢＩＧ５中文化工作我也差不多快完成了。等我實驗試用過，再來另寫一篇介紹吧。  
  
***本文為Security First製作的手機應用umbrella app正體中文化翻譯系列資料之一。目前仍為初稿狀態，虛心接受指正批評。原始的json資料格式配合app電子書的html編輯標籤，轉貼到部落格上排版混亂也欠缺原始圖檔請見諒。***  
**  
PGP for Linux 工具指南: Linux系統上加密電郵**  
  
![PGP](https://4.bp.blogspot.com/-umzkMEgm8o0/V35Mvc7hxeI/AAAAAAAAKWU/AagFUqRddTYWGT6wVWmD58tdrKK1M37CgCLcB/s1600/pgp.jpg)  
  
**學習內容:[電子郵件](umbrella://lesson/email)**  
**系統需求:** 網路連線, 運行Linux作業系統的電腦, 電子郵件帳號  
**本指南使用版本: **Linux: Debian 7.0 ("Wheezy"); Mozilla Thunderbird 24.8.1; Enigmail 1.6;GPG4Win 1.4.18  
**版權宣告:** 自由軟體；混合式自由軟體  
**Level:** Expert  
**Other reading:** [https://www.gnupg.org/documentation/guides.html](https://www.gnupg.org/documentation/guides.html)  
**需要時間:** 30-60分鐘  
**PGP 可讓你:**保護你的郵件通訊安全不會讓收件者以外的人所讀取;證明郵件是來自某人而不是任意偽造送寄者的訊息(要偽造寄出電子郵件並不困難).這兩者都是遇上被監控或是資訊被誤導時的重要防衛.  
  
**1.0 開始之前 **  
使用Pretty Good Privacy (PGP),需要先安裝某些額外軟體以相容於你所使用的電子郵件程式.你也需要創建保一個保存良好隱祕的私鑰.這組私鑰可以讓你解密給你的郵件訊息,進行數位簽證來證明你真的是寄件者.最後,你會知道如何傳播你的公鑰資訊給需要知道的人，好讓他們可以寄送給你加密的郵件以及確認你寄來的郵件.本指南讓你知道如何在Linux作業系統下使用Mozilla Thunderbird(雷鳥電子郵件軟體), 是一個開源流行的電郵軟體.你無法在網頁電郵如Gmail, Hotmail, Yahoo! Mail或Outlook Live上直接使用PGP，但你還是能利用這些網頁郵件來設定電腦上的雷鳥郵件接收寄送.**留意電子郵件的寄收兩端都必須使用PGP相容軟體才能發功效.**一般只在自己個人電腦上才使用PGP而不會在公用電腦上進行.幸好現在PGP已經普遍能在多數的桌面環境、手機設備上運作，你可以告訴對方如何找到適合他們安裝使用的版本資訊  
  
**2.0 安裝雷鳥, GnuPG 和 Enigmail **  
PGP是一個開放標準，這意謂著多種軟體皆可利用它. 這裏我們要介紹的PGP軟體叫作GnuPG.我們也需要在雷鳥上安裝Enigmail這個外掛插件，它可讓你在雷鳥上使用GnuPGP.下面的操作需要稍了具文字指令操作基礎.  
如果你使用的是紅帽發行的linux版本如 Red Hat or Fedora Core, 請打開終端器並執行以下文字指令:  
_sudo yum install gnupg thunderbird thunderbird-enigmail_  
如果你使用的是Ubuntu發行的linux版本如Ubuntu,  Linux  Mint, 為確認電腦上是否已安裝正確的軟體，請打開終端器並執行以下文字指令:  
_sudo apt-get install gnupg thunderbird enigmail_  
如果你使用的是Debian 版本的linux, 你會發現雷鳥在這裏被叫做“Icedove”. 對Debian而言,這完全是有道理但又有些模糊不清.除了名字之外,兩者是完全一樣的程式: 所以我們在本指南中就不再使用“Icedove”這個字眼，請以雷鳥來取代它, 一切應該都沒問題.  
透過終端器文字指令來安娤:_sudo apt-get install gnupg icedove enigmail_  
  
**2.1 設定Thunderbird**  
你已成功地安裝了電鳥, 請開啟它(從程式集選單下挑選開啟,或是打入它的名字搜尋). 你將會看到初次執行的簡易畫面出現 .![](http://self.jxtsai.info/tool_pgplin1.png)  
設定現有的電子郵件地址,請選點 "Skip this and use my  existing email“,然後輸入你的名字,電子郵件、密碼.![](http://self.jxtsai.info/tool_pgplin2.png)如果你使用的是流行的免費信箱如 Gmail,Thunderbird應可自動偵測其郵件設定，請點「繼續」 ”Continue“.**如果你啟動了Google二步驟驗證功能 (依你受到的威脅程度應該要啟用!) 在此你就無法使用一般的密碼登入Thunderbird.相反地你得先設定一個特別的應用程式專用密碼給雷鳥以便近用你的Gmail帳號.相關操作請見 [Google's 官網的指南](https://support.google.com/mail/answer/1173270?hl=en).**![](http://self.jxtsai.info/tool_pgplin3.png)如果不是Gmail 帳號, 你需要手動來調整郵件伺服器 IMAP/SMTP設定. 如果你不知道這些資訊,請聯絡你的電郵服務商,或詢問了解相關設定的技術人員 (辦公室的 IT人員,或使用相同郵件服務又懂技術的朋友;他們不必知道如何使用 PGP, 但你可以請教他們如何設定你電子郵件的伺服器 IMAP and SMTP設定 ).  
  
**2.2 設定Enigmail**  
Enigmail 是雷鳥上的一個外掛套件，其可讓你加密與解密PGP編碼的電子郵件，並且讓公鑰私鑰的處理更為方便.如果你安裝的是最新版本的Enigmail, 你應該會看到Enigmail簡易安裝過程.![](http://self.jxtsai.info/tool_pgplin4.png)如果沒看到,則可利用雷鳥的選單來叫出.點擊雷鳥視窗右側選單上的三條水平線.![](http://self.jxtsai.info/tool_pgplin5.png)第一個選項可讓你: 當需要加密電子郵件時有三種處理選擇.![](http://self.jxtsai.info/tool_pgplin6.png)程式預設的選擇是當你有別人的公鑰時, Enigmail將會加密你送給對方的郵件，但如果沒有收件人的公鑰則不會進行加密 .你也可選擇隨時利用公鑰加密寄出的郵件, 但這表示你得要有每個收件者的公鑰，而沒公鑰的收件人則要取消自動加密的功能只直接使用PGP.不知道哪一種選擇比較適合你的狀況，但我們相信便利的自動加密選項應是不錯的選擇. 如果你覺得困惑,就選擇「預設不要加密」“Don't encrypt my messages by default”.然後選擇「下一步」”Next“ .![](http://self.jxtsai.info/tool_pgplin6.png)現在你可以決定是否要對所有寄出的信件進行電子簽章. 利用PGP簽章你的電子郵件可以讓收件人檢查是否真由你送出這個郵件,而這個信件內容並未遭到竄改. 選擇開啟「預設簽章我的郵件」“Sign my messages by default”功能.這佪動作的不利之處在於, 它也讓人知道你使用PGP寄送電子郵件. [在某些國家](http://self.jxtsai.info/www.cryptolaw.org/) (包括中國，伊朗, 白俄羅斯, 以及某些中東國家) 使用未授權的加密，即使完全為私人目的,都是違法的,這讓你有理由不讓別人知道你使用PGP.  
接下來繼續點選下一步.現在你可以看到出現一個選項讓你來調整Mozilla Thunderbird底下Enigmail的變動.![](http://self.jxtsai.info/tool_pgplin7.png)點擊「細節」"Details"可以檢視這些變動的內容.如果你已預設使用PGP/Mime (我們稍後會介紹這個)，為了無間隙傳送，請不要選擇(或重啟)以下的功能:「取消缺流動型文字」”Disable flowed text“  
「以純文字格式檢視訊息」“View message body as plain text”,「不要用HTML格式撰寫郵件」 “Do not compose HTML messages”最後一個選項是預防加密或解密電子郵件的潛在問題.注意選取了這個框框後會移除文字的格式，如粗體、底線或顏色.檢視過這些變動後,現在可以選擇「OK」.現在你可以開始來創建自己的私鑰與公鑰.  
  
**2.3 創建私鑰與公鑰**  
完成安裝與設定Enigmail外掛套件後. 你會進入到創建自己私鑰與公鑰的選項中.這是假設你過去尚無任何私鑰.![](http://self.jxtsai.info/tool_pgplin8.png)請選擇「下一步」.除非你設定了多個電子郵件帳號, Enigmail 一般會選擇你已經設定完畢的那組.首先你需要有一組高強度的密語來管理你的私鑰. 請見**[密碼課程](umbrella://lesson/passwords)**以了解相關資訊.  
Enigmail會展示有關私鑰的資訊以及其設定方法.我們建議採4096-位元長度的密鑰. 選擇「下一步」.![](http://self.jxtsai.info/tool_pgplin9.png)**你的密鑰可能過了一段時間後會到期; 這種情況下, 有些人會停止使用過期的密鑰來傳送郵件, 所以你也不會收到任何警告或解釋原因的訊息.或者你希望註記上日期來提醒你即將到期的問題.**它可以延長現有密鑰的到期日，也可以用另一組新密鑰來替換.但兩者都需要通知收件人讓他們獲得更新的密鑰資訊;而目前這套軟體尚無法自動作到這點.所以你得自己留意;如果你不認為自己可以搞定此事，不妨考慮設定一組永不過期的密鑰。如果你不再保有這組私鑰或不再使用PGP，某些人可能還是會利用這個資訊來聯絡你.Enigmail將會在完成前産生一組密鑰, 此時會出現一個小視窗詢問你是否要産生一個取消證明. 這個取消證明的重要之處在於可以讓你的私鑰與公鑰成為無效.記住只是刪除了私鑰並不會自動取消公鑰的效力，而這會讓他人寄給你加密電子郵件但你卻無法解密.![](http://self.jxtsai.info/tool_pgplin10.png)點選「産生證明」“Generate Certificate”.這時會出視新視窗讓你選擇儲存取消證明的位置. 你可以把它存在電腦硬碟上，但我們建議最好是把這個檔案存在一個用不到的USB記憶卡並把它保存在一個安全的地方. 最好把電腦上的取消證明檔案刪除，以避免發生意外的消取事件.更好的作法是把這個檔案存在一個分開的加密磁碟上.完成選擇檔案儲存的位置後請點擊儲存鍵.現在Enigmail會再次給你關於取消證明檔案進一步的資訊.點擊“OK”.最後你終於完成了公鑰私鑰的創建，請選擇完成鍵.  
  
**2.4 可選步驟  
2.4.1 顯示長密鑰IDs**  
這個步驟完全視個人需要做選擇但它們可以在使用OpenPGP和 Enigmail有所幫助. 簡言之, 密鑰ID 是指紋碼的一小部份.當需要認證公鑰是否屬於某人時，指紋碼是最好的方法.改變預設的顯示讓讀取指紋碼證明更為容易.，在Enigmail選項下點選設定鍵中的密鑰管理部份.![](http://self.jxtsai.info/tool_pgplin11.png)將出現一個視窗顯示二欄位:姓名與密鑰ID.![](http://self.jxtsai.info/tool_pgplin12.png)在最右邊有一個小按鍵.請點擊此鍵以便設定欄位.解除Key ID 選項然後點選指紋碼選項.![](http://self.jxtsai.info/tool_pgplin13.png)現在移動滑鼠到每一欄位頭部的線端(就是的右邊最上方的密鑰表)來改變指紋碼欄位的長度,然後拖曳這條線到左邊.保持往左移動直到你能看到所有的Key ID,就像這樣:所有的欄位就長成這樣:![](http://self.jxtsai.info/tool_pgplin14.png)現在你可以正常地收送一般與加密郵件了.接下來你將會被介紹如何找到要交換加密郵件的對象.  
**PGP 不能完全加密你的電子郵件所以送件人和收件人的資訊要加密**. 但加密收件人和收件人可能會破壞電子郵件.使用雷鳥的外掛套件the Enigmail 可以簡單地加密和解密你的郵件內容.  
  
**3.0 讓別人知道你有使用PGP**  
**a) 讓別人知道你有使用PGP處理電郵**你可以簡單地把自己的公鑰以附件方式寄給其它人.在雷鳥軟體下點搫「撰寫」“Write”.填入地址以及信件主旨,例如像:我的PGP公鑰,從Enigmail選單選擇「附加我的公鑰」”Attach My Public Key“.![](http://self.jxtsai.info/tool_pgplin15.png)你現在可以寄了收件人郵件而對方可以收到下載你的公鑰.**如果用這個方法,最好讓收件人可以透過其它管道認證你的公鑰指紋碼，以防電子郵件可能已遭到攔截或破壞.**  
**b) 在你的網站上讓別人知道有使用PGP**除了透過電郵讓別人知道外,你可以把你的公鑰放在自己的網站.最簡單的方式是把檔案上傳並加一個連結. 本指南就不介紹如何完成這些步驟，但以後你會知道如何滙出你的公鑰檔案.在Enigmail選項下點選設定鍵中的密鑰管理部份.將你的證明用粗體字突顯,然後用滑鼠右鍵來開啟選單，然後選擇滙出公鑰到檔案中.![](http://self.jxtsai.info/tool_pgplin16.png)有三個按建的小視窗將會出現.請選擇“Export Public Keys Only”按鍵.![](http://self.jxtsai.info/tool_pgplin17.png)**確認你不要按到“Export Secret Keys”按鍵，因為這個會讓其它人模倣你如果他們能猜出你的密碼 .**接下來會出現讓你存檔的視窗. 為了以後可以更容易找到這個檔案，請把它存在文件目資料夾下.現在你可以盡情使用它了.  
**c) 上傳到密鑰伺服器**密鑰伺服器讓人更方便來找到與下載公鑰.大部份的公鑰伺服器之間都有同步功能,這表示上傳的公鑰最後都會傳到其它伺服器.雖然把你的公鑰上傳到密鑰伺服器是一個方便的方法讓其它人知道你有一個公開的PGP證明,但由於密鑰伺服器本身運作的性質,一旦把公鑰上傳後將無法刪除,你只能註記它們已經被取消.**上傳公鑰到伺服器之前,最好先考慮你是否要讓全世界知道你有一個公鑰因為這個資訊之後將無法取消.**如果你選擇上傳公鑰,你要再回到Enigmail的密鑰管理視窗下.點擊密鑰伺服器選單再選擇上傳公鑰的選項.![](http://self.jxtsai.info/tool_pgplin18.png)  
  
**3.1 找到也使用PGP的人**  
**a) 透過電子郵件取得公鑰**你可以透過別人寄出的電郵附件檔案來取得其公鑰.![](http://self.jxtsai.info/tool_pgplin19.png)留意在郵件下方的附件檔. 右擊該附件然後選擇「滙入公開PGP公鑰」“Import OpenPGP Key”.一個小視窗會開啟讓你知道其滙入的結果.點選“OK”.如果你再次開啟Enigmail的密鑰管理視窗, 可以檢視其結果. 你的PGP密鑰是粗體字因為你同時有私鑰和公鑰.而剛才匯入的公鑰就不是粗體字因為它並不包含私鑰.![](http://self.jxtsai.info/tool_pgplin20.png)  
**b) 取得公鑰檔案**你可能從網站下載或某人透過聊天軟體給你公鑰檔案二.在這種情況下假設下載的檔案存放在下載的資料夾中.開啟Enigmail密鑰管理視窗然後點選檔案選單.從其選單中選擇「從檔案中滙入公鑰」“Import Keys from File”.這個公鑰檔案可能有不同的副檔名諸如.asc,.pgp,.gpg 等等，選擇該檔案然後點選開啟鍵，會打開一個小視窗顯示滙入的結果.再點選“OK”.  
**c) 從密鑰伺服器上取得公鑰**密鑰伺服器是一個很有用的方法來取得公鑰.要試著找他人的公鑰，請打開密鑰管理員然後點擊「密鑰伺服器」選單，選擇「搜㝷密鑰」”Search for Keys“.![](http://self.jxtsai.info/tool_pgplin21.png)它會彈出一個有搜㝷欄的小視窗.你可以透過電子郵件地址或部份地址或姓名來找.例如你可以找含有”eff.org.“字串的證明![](http://self.jxtsai.info/tool_pgplin22.png)稍後一個較大的視窗會出現許多選項.如果你往下滑動會注意到有些證明是斜體字且呈暗灰色. 這一類的證明多半是已取消或是過期了.![](http://self.jxtsai.info/tool_pgplin23.png)  
讓我們以Danny作例子, 他有一個過期或註消的證明也有一個仍然有效的證明.請勾選其有效的證明然後按下OK鍵.![](http://self.jxtsai.info/tool_pgplin24.png)某些案例中有人可能有多個有效的證明. 注意也有可能是非本人所上傳的公鑰而該公鑰並不是該電子郵件的使用者或是並無關聯.這種情況下,查證指紋碼就變得格外重要.一個小的提醒視窗會彈出來讓你知道是否成功，然後Enigmail的密鑰管理員會顯示出新增的證明:![](http://self.jxtsai.info/tool_pgplin25.png)  
  
**4.0 傳送PGP加密郵件**  
現在你可以寄出加密郵件給特定的收件人.在Mozilla Thunderbird選單視窗下點擊「撰寫」"Write"以打開新視窗.寫下你的信件內容,並輪入收件者.為了測試,請選擇一個你已有其公鑰的收件人. Enigmail會自動偵測且加密電郵(你可以從郵件下方右側的金色鍵知道其為加密內容).![](http://self.jxtsai.info/tool_pgplin26.png)**注意，信件的主旨欄不會被加密,所以請選擇一些看來無害的字眼, 例如hello等等**當你按下送出鍵時,會出現一個要求你輪入PGP密鑰密碼的視窗.記住這密碼不是你的電子郵件密碼!輪入密碼後按OK，之後你的郵件就會被加密送出.郵件的內文會被加密和轉換. 例如我們上面原本的文字會變成如下:![](http://self.jxtsai.info/tool_pgplin27.png)  
  
**4.1 接收PGP加密郵件**  
讓我們走一遍當你收到加密郵件時會發生的狀況.首先,請開啟這則郵件.會出現詢問密碼的小視窗.記住這密碼不是你的電子郵件密碼!選擊“OK”鍵。![](http://self.jxtsai.info/tool_pgplin28.png)好了，現在這個郵件已被解密了![](http://self.jxtsai.info/tool_pgplin29.png)  
  
**5.0 取消PGP密鑰**  
**a) 透過Enigmail 介面來取消PGP密鑰**Enigmail所建立的PGP密鑰會在5年後自動到期. 所以如果你遺失了所有的檔案,你只有期望認識的人會在過期後來詢問你另一組公鑰.你也有其它理由在PGP密鑰到期前把它先取消掉.例如你要建立一組新的，更難破解的PGP密鑰.最簡單的方法是透過Enigmail的密鑰管理員來取消你自己的PGP密鑰.用滑鼠右鍵來選取你的PGP密鑰(它是粗體字), 再選擇「取消密鑰」“Revoke Key” 選項.![](http://self.jxtsai.info/tool_pgplin30.png)此時會彈出一個新視窗讓你知道發生的狀況被要求你的確認.請選擇「取消密鑰」 “Revoke Key”.![](http://self.jxtsai.info/tool_pgplin31.png)The password window opens密碼視窗將會開啟,請打入你的PGP密鑰密碼然後點選“OK”.現在會再有一個新視窗出現以知會你成功取消.點擊"OK".當你重回Enigmail的密鑰管理員視窗，你將注意到原有PGP密鑰的變化，它現在變成了灰暗的斜體字。![](http://self.jxtsai.info/tool_pgplin32.png)  
**b) 透過取消證明來取消PGP密鑰**如之前提到, Enigmail所建立的PGP密鑰會在5年後自動到期。所以如果你遺失了所有的檔案,你只有期望認識的人會在過期後來詢問你另一組公鑰.如之前提到, 你或許有好理由在PGP密鑰到期前把它先取消掉.同樣地,其它人也有好理由在PGP密鑰到期前把它先取消.你或許會收到來自友人的取消證明以通知你他們將取消原有的密鑰。前面所提的部份你或許已經注意到當使用Enigmail的密鑰管理員來取消密鑰時，Enigmail 本身會産生和滙入一個取消證明. 既然你已有一個取消的證明，你可以用它來取消你自己的密鑰.啟動Enigmail的密鑰管理員然後點選選單檔案下的「滙入密鑰」“Import Keys from File”功能![](http://self.jxtsai.info/tool_pgplin33.png)此時會彈出一個視窗來讓你選擇取消證明，點選正確的檔案再按“OK”，你會得到一個消取證明已成功滙入且密鑰已被取消的通知。選擇"OK".![](http://self.jxtsai.info/tool_pgplin34.png)當你選擇"OK"之後,你會被帶回到Enigmail的密鑰管理員底下，可以看到你所取消的密鑰現在已變成了灰暗的斜體。![](http://self.jxtsai.info/tool_pgplin35.png)如果取消的是你自己的密鑰,以及你之前上傳到密鑰伺服器上的公鑰,你將要重新上傳已被取消的密鑰到伺服器上好讓其它人知道不要再使用這組公鑰.現在你有了所有適當的工具，試著傳送一封PGP加密的郵件吧。

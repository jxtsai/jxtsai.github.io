---
author: jx tsai
comments: true
date: 2016-06-17 08:59:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/06/17/mailvelope-webmail%e5%8a%a0%e5%af%86%e5%b7%a5%e5%85%b7-%e4%bd%bf%e7%94%a8%e4%bb%8b%e7%b4%b9/
slug: mailvelope-webmail%e5%8a%a0%e5%af%86%e5%b7%a5%e5%85%b7-%e4%bd%bf%e7%94%a8%e4%bb%8b%e7%b4%b9
title: Mailvelope--webmail加密工具--使用介紹
wordpress_id: 62
categories:
- encrypt
- localization
- opensources
- privacy
---

最近做完了[mailvelope](https://www.mailvelope.com/)這個瀏覧器上的外掛加強元件的正體中文化初稿，於是為文稍微介紹一下這個軟體。  
  
之前有提過[GNU ＰＧＰ（pretty good privacy）如何使用](http://self.jxtsai.info/2015/09/gpg.html)、以及制作了Security First umbrella app 的中文化初稿裏也有關於「[ＰＧＰ for linux 工具指南](http://self.jxtsai.info/2016/06/pgp-for-linux.html)」的介紹。  
  
![mailvelope](https://1.bp.blogspot.com/-qn77H1WGKr4/V30enKYRDUI/AAAAAAAAKQE/MqbyroHZ7SUmrZUewsp2kQDVq26t6zoDQCLcB/s1600/mailvelope.jpeg)雖說ＰＧＰ或相關電子郵件加密安全的開發者已經大力地改善了其在個人電腦端或智慧型手機上的郵件/檔案加密操作介面，但至今仍鮮少有人會真的在寄電子郵件時先使用指定收件對像的加密處理與信件發出認證步驟。這要說是因為：１）幸好在這個年代裏，我們所處的台灣已相對的自由開放，不再有對於言論打壓的恐懼呢？　２）我們並不知道國家/跨國企業對於數位科技偵測實質通訊內容或僅以為收集的是後設（詮釋）資料（metadata），又或者是３）我們日常所進行的通訊本身實無須有保密機密價值只是日常的工作庶務處理或問題交流，沒什麼獨門可賺大錢的商業機密或是沒有推翻政府謀畫隨機殺人、冒著危險吹哨黑心企業/政府違法內幕等高敏感的內容。４）網路犯罪集團可能會駭入我的帳號來閱讀我的電子郵件內容。以我個人的現狀來評估一下我的數位通訊[「受威脅模型」](https://ssd.eff.org/en/module/introduction-threat-modeling)到底是哪一個程度，我大概沒有第１、第３、第４的狀況，但會介意的應該是第２點：擔心國家/跨國企業對於數位科技偵測實質通訊內容或後設資料（metadata）的收集)，但硬要說這點憂慮是否對我造成了實際損害，不然我在哀什麼。雖然看似沒有造成什麼財物與身體損害，但我就是不爽在不知情未充份同意的狀況下，個人資料並他人收集使用。  
  
所以呢，本文就要來介紹一下電郵通訊加密的另一個方便工具Mailvelope，據其官網上的介紹，其是以 OpenPGP 標準下 javascript程式語言OpenPGP.js為基礎開發的網頁版電子郵件加密外掛附件(嗯，其實我不太知道ＰＧＰ、ＧＰＧ之間的差異，其加密演算法的強度如何)。稍知javascript者都知道它一開始是應用於網頁前端開發，希望能提高網頁互動呈現的程式語言。而鑑於過去十年來gmail的流行，outlook(hotmail)、yahoo等服務商也把容量越增越大，電子郵件用戶也越來越習慣用瀏覧器讀取寄送郵件，也把郵件長年地留在這些供應商的郵件伺服器上，方便查找。至少以我個人的習慣，早已沒在使用獨立的電子郵件軟體。所以當資安手冊說：這樣把郵件留在伺服器上，萬一有天被逮捕其郵件可能被執法單位搜索查看作為證據（這裏指的被補應該是指在某些仍然高壓統治國家裏對於社運人士的打壓），或是資安手冊教我們如何在ThunderBird上安裝enigmail 外掛以使用電郵加密時，我個人實在無法把習慣從webmail翻轉回email client。  
  
而Mailvelope的出現，有稍解決了一點這樣的不便。以下就來示範一下它的操作:  
  
１.　目前它有支援Chrome與Firefox ,看使用者習慣哪一個瀏覧器就去安裝它的Mailvelope外掛（官網上都有連結）。安裝完畢後，則會在瀏覧器的工具列上看到出現一個新的小掛鎖圖示。  
  
2. 點開Mailvelope小掛鎖圖示後，再選取最下方的「Option」即會自動在瀏覧器中開啟一個新分頁，裏面可以再做一點細部設定。當然最重要的是就是「Key Management」,在這個地方可以輸入自己的私鑰以及收件人的公鑰。如果尚未專屬自己的私鑰，則可以在「Generate Key」生成一組新的密鑰。（一組內即有二把公鑰與私鑰）  
![new tab](https://1.bp.blogspot.com/-I6VB8fKPubk/V32S0wM-2oI/AAAAAAAAKRg/nsvZuLA8Nngp7LOVJr9Isdd-DyvbP1H1QCLcB/s320/new-tab-1024x621.png)  
  
3. 其它的設定，因為我是先以gmail為實驗，故其它設定倒是都沒改更。  
  
４. 回到gmail 的網頁底下，點「compose」要來寫一封新的電郵內容，一般在gmail就會彈出一個寫信的小視窗，而在裝了Mailvelope外掛以後，這個小視窗裏的右上方會出現一個紙筆的小圖示。點這個小圖示就會再彈出一個Mailvelope的外部編輯器。請在這個有Mailvelope小圖為浮水背景的外部編輯器裏，打入你的機密電子郵件內容。信件打完後，當然就按右下角最右邊的「Encrypt」來對這個內容進行加密。  
![editor](https://4.bp.blogspot.com/-vkut9ZEMWSQ/V30drL7lJXI/AAAAAAAAKPs/9cdC_rLoSPEyc94-TlRUYzkHdLmS2J_1ACLcB/s320/editor-1024x525.png)  
  
5. 接下來會彈出一個視窗，詢問這封機密郵件的收件人是誰，好利用她的公鑰（假設已存入在「Key Management」之下）來對此訊息加密。官網的文件是建議，也把自己列為加密對像，這樣才方便日後在寄送備份資料夾中可以用私鑰來解密自己送出什麼樣的機密信息。選好要指定的加密收件對象後，軟體就會自動進行加密動作，完成後，原來打入的訊息就變成了一串奇奇怪怪的東西貼在Mailvelope的外部編輯器裏，不要擔心，反正就是按右下角的「Transfer」 。  
![encrypt](https://2.bp.blogspot.com/-49WCrbikzTo/V30eUwcVOdI/AAAAAAAAKP4/MQOIbcHo6KYd9WWtDXTbqM5jLkZBaRkHACLcB/s320/encrypt-850x503.png)  
  
  
6. 最後Mailvelope外部編輯器會被這串加密過的內容自動貼到gmail底下的郵件編寫視窗的郵件內文中，而Mailvelope編輯視窗則會自動關閉。接下來要做的，就是照正常在gmail介面底下的寫信寄信方式，把這個郵件寄出給對方吧。  
  
７. 如果好奇自己寄出的加密郵件是否有成功，可以到「寄件備份」下，打開寄出的加密郵件，然後它會詢問可以解開這封郵件密鑰的密碼（前提是有照前面第５個步驟把自己也列為加密對象,才可以進行解密，否則它會說找不到可以解開這封機密內容的私鑰）。正確輸入密碼後，它會被自動把訊息解密還原了。  
![key](https://1.bp.blogspot.com/-xJJymd4KJPI/V30ecUGn-XI/AAAAAAAAKP8/1qI8ziMgys8oZ-fxnX84fJRWEv4nT0qwACLcB/s320/key.png)  
以上就是Mailvelope的使用介紹。還算蠻方便的,希望我作的中文語言包初稿也能早點確認後被放到軟體中。另外，如果真有人要寄加密的資料給我，我的公鑰資訊在[這裏可以找到](https://www.jxtsai.info/blog/me)。  
  
又註，看到自由軟體基金會2014年所製作的資訊圖表說明使用ＧＰＧ密鑰進行電子郵件加密保護的運作介紹。覺得蠻不錯的，故轉貼過來。  
  
[![EmailSelfDefense ](https://static.fsf.org/nosvn/enc-dev0/img/en/full-infographic.png)](https://emailselfdefense.fsf.org/en/infographic?pk_campaign=email_self_defense)

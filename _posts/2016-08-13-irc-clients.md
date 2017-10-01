---
author: jx tsai
comments: true
date: 2016-08-13 11:02:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/08/13/irc-clients-%e4%bd%bf%e7%94%a8%e8%a8%98%e9%8c%84/
slug: irc-clients-%e4%bd%bf%e7%94%a8%e8%a8%98%e9%8c%84
title: IRC clients 使用記錄
wordpress_id: 29
categories:
- dotlife
- opensources
---

IRC 算是老牌的網路聊天室，尤其在開發者社群的使用其實應該是一直歷久不衰。但對於非技術型的末端使用者，則不易發覺它的樂趣與妙用之處。（好吧，我承認我一直搞不懂它好玩在哪裏）。最近試著再重摸IRC的使用方法，本文是自用的參考筆記。  
  
我記得自己很久以前是透過在FireFox底下的外掛來進入IRC聊天頻道，近來也發展了各式支援網頁webchat協議的IRC平台（要直接透過瀏覧器使用網頁版的IRC，可參考[g0v.tw所整理的中文介紹](https://github.com/g0v/dev/wiki/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8-IRC)。）但我想人總是要試著一點不同的東西，因此試著在ubuntu 底下的IRC客戶軟體--XCHAT, KONVERSATION, HexChat。安裝這些軟體並不困難，都是透過ubuntu software center來進行安裝，比較大的問題是在軟體安裝好之後的設定細節。  
  
[ＸCHAT](http://xchat.org/):是不少linux使用者推薦的老牌IRC軟體,不過自2010年以來已經6年多沒更新了。  
１. 一進入xchat第一個畫面就是先確認你要使用哪一個ＩＲＣ伺服器以及上方個人的匿稱資訊。  
![](https://2.bp.blogspot.com/-L_Q4cioesx0/V60niRPvxqI/AAAAAAAAKuY/sTlm1X4ouu0ZKW7OwexO5sGfbX5fMCOAQCLcB/s1600/networklist.png)  
因為我要進入的聊天室放在freenode.net，當然是挑選它囉。不過因為xchat久未再更新，內建的ＩＲＣ伺服器的資訊有點舊了，例如其對於freenode的資訊設定還是：irc.freenode.net。　但其網域名已改成了： chat.freenode.net, 故要手動更新此資訊才能成功連線。如果要使用安全加密的連線（SSL）,則輸入：irc.freenode.net/6697,並勾選底下：“USE SSL for all the servers on this network”。無SSL的端口則是irc.freenode.net/6667。理論上兩者都可成功連線登入才是，但不知為何，我只有在設定SSL連線狀況下才能成功進入IRC。  
![](https://4.bp.blogspot.com/-y6X5COmb4pw/V60pNC_3EUI/AAAAAAAAKuk/LV8bFaX3NvgNAV_7PCuvXjnIc0b0l9EOACLcB/s1600/freenode.png)  
  
雖然作了freenode.net伺服器資訊的更新，但還是一直無法成功地連結IRC伺服器。且傳回以下訊息：　  
Notice -- You need to identify via SASL to use this server  
* Closing Link: 1-173-99-83.dynamic.hinet.net (SASL access only)  
* Disconnected (Remote host closed socket).  
[![](https://2.bp.blogspot.com/-p9xweQ98-HM/V63bUdEMGkI/AAAAAAAAKvI/vV34Pwpee1UPDXZ47tevsTFWSNQemcSKwCLcB/s1600/sasl.png)](https://2.bp.blogspot.com/-p9xweQ98-HM/V63bUdEMGkI/AAAAAAAAKvI/vV34Pwpee1UPDXZ47tevsTFWSNQemcSKwCLcB/s1600/sasl.png)  
  
查了一下freenode 官網的資料，原來它是要求使用者先完成其匿稱與密碼的註冊登記才能成功連線。咦，連都連不上去了，怎麼註冊自己專用的匿稱和密碼咧？於是只好先透過webchat的方法，登入到其ＩＲＣ伺服器。可以看到它的網頁登入畫面中，並無要求使用者須輸入密碼的欄位。  
![](https://1.bp.blogspot.com/-RpuTM9utoDE/V60r18pD0mI/AAAAAAAAKuw/6FV6UeNU3kwHmYO6HUt1sZu0mdIGzLT_QCLcB/s1600/webchat.png)  
  
如何註冊常用匿稱、修改匿稱等  
![](https://3.bp.blogspot.com/-9t4bIqWoF6A/V60sOLAJl-I/AAAAAAAAKu0/-UxzTm4cqXodpQ37KtYG-37qpSo9cukUACLcB/s1600/webchannel.png)  
請在進入IRC之後，最下面游標會動的文字欄當中輪入相關指令，例如要綁定自己的常用匿稱與密碼  
/nick nickname #修改原登入匿稱, nickname　即為新取的匿稱。不過如果所在的聊天室當中，已有人先取了同樣的匿稱，則無法成功變更。  
  
好了，登入webpage irc最主要的目的是幫自己綁定一個專用的帳戶（匿稱）與密碼，故在同一個文字輸入欄中，打入以下指令：  
/msg NickServ REGISTER password youremail@example.com  ##password 請輪入自己偏好的密碼;  youremail@example.com 也要改為自己的信箱，以便接收待會系統寄出的認證信件。　如果想取的匿稱已被它人使用了，就會叫你再更改。  
很快地會在自己的信箱收到一封確認的郵件，只要把信中叫你在文字指令列打入的那行訊息（類似　/msg NickServ VERIFY REGISTER name vzfq$#$@#）之類的，貼到最底下文字列，完成認證手續，就可以透過IRC client的SASL連線要求。  
  
接下來再回到IRC client軟體，這時候就可以把自己在freenode.net登記的用戶名與密碼資料存在IRC server登入資料中（nickserver password）。此時再作連線，基本上就可以很順利地登入到chat.freenode.net某一台伺服器，這時就會彈出一個視窗如下下圖，詢問你是否要加入某一個頻道。如果不知道該進入聊天室，又很無聊地有時間去串門子到處亂看看，可以在此時點開下方“Open Channel-List window”，就會彈出目前在chat.freenode.net上面的聊天頻道清單，從最上方的資訊可看到大約有34萬用戶正掛在10245個聊天室頻道中，目前這些聊天室的主題多以開發者社群居多。（「早年」我使用時，也許因為當時網路聊天即時通訊還不是很方便，所以某些社會、人文類的社群聊天頻道還不少哩）  
![](https://3.bp.blogspot.com/-gBa9YJa2Y34/V66AOCgVGDI/AAAAAAAAKvc/pBhuJviDBIw43ZB6acYYTnj7oDBrpDEwACLcB/s1600/nick.png)  
![](https://3.bp.blogspot.com/-iRZVcXysbZo/V66AtAng6BI/AAAAAAAAKvg/_oGzKZxWY7szcYGwumu372K43A3cjqaMACLcB/s1600/login.png)　  
![](https://4.bp.blogspot.com/-gJOrX5-yLac/V66CICTY94I/AAAAAAAAKvs/J46ieZuj0BAdg8MXVrQt_yassE7WZR71QCLcB/s1600/channel-list.png)　  
  
在IRC頻道中，別把它當成一對一的約炮聊天工具（雖然它也有一對一私下聊天功能），一個聊天室頻道，通常就是大家都靜靜地掛著。也許偶而會有人闖入發問了一道和主題有關的問題（ex javascritpt套件、python模組使用之類的問題），或者有時候是社群中約好了時間要一起在IRC開會討論某些議題的場合,但更多的恐怕是安靜的沈默，尤其是台灣中文社群，似乎大家改用了其它線上討論聊天工具（telegram, slack?）。反正我覺得就是長期習慣低調的我，就是默點走進一個頻道（或多個頻道），也不必打什麼招呼，然後就靜靜地掛著待著，看著其它人偶而「熱烈」的討論。  
  
除了這種多少帶著圖型介面的環境外，我也嚐試著使用終端機下純文字指令介面的IRC軟體，這類據說最被推薦的是irssi。我在安裝後，也同樣是在SASL登入設定上發生了撞牆狀況。目前還沒能解決。  
[![](https://3.bp.blogspot.com/-nzSCtsjlsyA/V674qXnFVQI/AAAAAAAAKv8/d7eUSKg-T-EUuu15MHGQhUtBmuInQVBNQCLcB/s1600/irssi.png)](https://3.bp.blogspot.com/-nzSCtsjlsyA/V674qXnFVQI/AAAAAAAAKv8/d7eUSKg-T-EUuu15MHGQhUtBmuInQVBNQCLcB/s1600/irssi.png)  
  
最後，開源且支援不保留記錄與點對點加密功能的[即時聊天軟體Pidgin](http://self.jxtsai.info/2016/05/pidgin.html) 本身也有支援IRC功能，這篇介紹雖然[是英文，但圖片說明很清楚](http://blog.artofmemory.com/how-to-use-irc-pidgin-tutorial-3538.html)，故我就不再重覆多講。  
![](https://1.bp.blogspot.com/-ExXdiAYtDCg/V67-L2cc1FI/AAAAAAAAKwM/CEQu2B8-cq0zd5J7XLbncVGlbAmMtvsYQCLcB/s1600/pidgin1.png)  
IRC 新手入門指令 ： [IRC Class - Basic IRC Commands](http://www.ircbeginner.com/ircinfo/ircc-commands.html)  
稍簡單整理如下：  
/join #channelname ##加入某聊天室  
/msg  ##傳私人訊息給某人，聊天室其它人不會看到  
/list  ##列出伺服器上的所有聊天室頻道清單  
/me   ##向其它顯示自己的狀態  
/part 離開聊天室  
/partall 離開所有聊天室  
/ignore   ##忽視某人的訊息，尤其是來亂的傢伙  
/chat   ##據說也是傳私人訊息功能  
  
  


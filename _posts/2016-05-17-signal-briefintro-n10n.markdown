---
author: jx tsai
comments: true
date: 2016-05-17 10:18:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/05/17/signal-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97/
slug: signal-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97
title: SIGNAL 工具指南
wordpress_id: 77
categories:
- localization
- opensources
- Security First
- umbrella app
---

同樣還是[Security First's umbrella app ](https://secfirst.org/)的正體中文化初稿。這篇介紹的是Signal用於iphone上的安全加密語音通話軟體。從沒用過iphone無從評論。據說Signal可以和運行安卓手機的Redphone跨平台安全通話，另見前一篇：[RedPhone的工具指南](http://self.jxtsai.info/2016/05/redphone.html)中文篇。  
  
***本文為Security First製作的手機應用umbrella app正體中文化翻譯系列資料之一。目前仍為初稿狀態，虛心接受指正批評。原始的json資料格式配合app電子書的html編輯標籤，轉貼到部落格上排版混亂也欠缺原始圖檔請見諒。***  
  
**Signal 工具指南**--iPhones專用的語音電話加密軟體  
  
![Open-Whisper-Systems-Releases-Signal-into-the-Google-Play-Store](https://3.bp.blogspot.com/-hELGNhc9HQA/V35CvPYVhEI/AAAAAAAAKVM/BvCCAfU5XykuyTb3-GSul8fl6g0UCQgVACLcB/s320/Open-Whisper-Systems-Releases-Signal-into-the-Google-Play-Store.png)  
**學習內容:[撥打電話](umbrella://lesson/making-a-call)**  
**下載處:** 本軟體可從 [Apple App Store](https://itunes.apple.com/us/app/signal-private-messenger/id874139669?mt=8)軟體商店下載  
**系統需求:** iOS 7.0 以上版本.相容於 iPhone, iPad, 與 iPod touch.  
**本指南所用版本:** Signal Private Messenger 1.0.5  
**版權宣告:** GPLv3  
**程度:**初學者-中級  
**其它參考資料:** [https://whispersystems.org/blog/signal/](https://whispersystems.org/blog/signal/);[http://support.whispersystems.org/](http://support.whispersystems.org/)  
**所費時間:** 15-20分鐘  
**使用Signal 可讓你:**在無線網路或資料傳輸時用你一般的電話號碼來撥打加密語音電話  
注意:雖然它是使用你的手機門號當作聯絡人識別;但通話卻常常是透過資料傳輸進行，因此通話雙方的設備都得要有網路連線才行.Signal只能在雙方皆安裝使用 Signal 或是 Redphone (安卓手機用)軟體的情況下才能進行加密功能。(後者請見**[RedPhone 工具指南e](umbrella://lesson/redphone)來了解其如何操作)**  
  
**1.0 如何安裝Signal**  
**第1步:** 下載與安裝“ Signal :Private Messenger“  
在你蘋果設備進入 App Store後搜尋「Signal」. 選擇由Open Whisper Systems開發的“Signal ： Private Messenger”.點擊下載程式並同意接受iTunes Store 服務條款.這個軟體將會自動下載完成安裝。點擊軟體來開啟其運行。  
**第2步:** 註冊和認證你的手機號碼,你將會看到如下的螢幕畫面:![](http://self.jxtsai.info/tool_signal1.png)  
輸入你的手機號碼後點擊註冊鍵。要認證你的號碼，你會收到一則 SMS 文字簡訊其中有6碼字符; 請將這組確認碼打入要求的地方. 如果你一直沒能收到確認碼的簡訊,也可以透過接收語音電話方式來取得確認碼.輸入確認碼後點擊「確認」。  
  
**2.0 使用 Signal**  
為了能使用 Signal, 你所欲通話的對象也要安裝好Signal (安卓使用者則是RedPhone)。如果你試著利用Signal撥打電話給某人但他們還沒安裝過這個軟體,這時此應用程式會詢問你是否要主動透過SMS簡訊邀請對方也使用Signal,否則它不能讓你透過這個軟體完成打電話動作.![](http://self.jxtsai.info/tool_signal2.png)  
  
**2.1 如何開始使用加密語音電話**  
要打加密電話給某位聯絡人,你必須使用Signal 應用本身的撥號介面。(這和Android用的 RedPhone不太一樣,RedPhone可讓人透過一般手機撥號系統來打加密電話)  
一旦通話建立了,雙方將可以看到一對隨機的文字資訊. 這組文字可讓你來確認身份和其它使用的密鑰是否吻合，也就是所謂的密鑰認證方式.![](http://self.jxtsai.info/tool_signal3.png)  
最可靠的通話者認證方法是透過頻外授權out-of-band authentication來比對文字. 如果你認得出對方的聲音，也可以大聲地念出你被分配到文字組合來比對確認,但厲害的攻擊者也許能夠竊聽到而進行破壞。比對的文字必須要一模一樣才行。

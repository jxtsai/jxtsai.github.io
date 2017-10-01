---
author: jx tsai
comments: true
date: 2016-05-16 00:10:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/05/16/redphone-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97/
slug: redphone-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97
title: REDPHONE 工具指南
wordpress_id: 78
categories:
- android
- localization
- opensources
- Security First
- umbrella app
---

無止無盡的umbrella app中文化初稿。sigh....  
我的廢癆：紅色電話這個軟體我兩三年前也試著在自己的智慧型手機上安裝過，果然在手機聯絡簿上沒顯示任何一名認識者也在其手機上安裝這套軟體。果然人還是活得不知不覺才會愉快點啊。  
  
***本文為Security First製作的手機應用umbrella app正體中文化翻譯系列資料之一。目前仍為初稿狀態，虛心接受指正批評。原始的json資料格式配合app電子書的html編輯標籤，轉貼到部落格上排版混亂也欠缺原始圖檔請見諒。***  
  
**RedPhone 工具指南**--Android 手機上的通話加密軟體  
![redphone](https://1.bp.blogspot.com/-vR4A9s2uPf0/V35DbBDx8CI/AAAAAAAAKVQ/S0VPNdvh3Ds3oWcuyEZA1gAVcluRA5kGQCLcB/s1600/redphone.png)(照片出處：[RedPhone: An Open Source Encryption App For Your Calls](http://www.gsmnation.com/blog/2013/06/06/redphone-an-open-source-encryption-app-for-your-calls/))  
  
**學習內容**:[撥打電話](umbrella://lesson/making-a-call)  
**下載處:** https://whispersystems.org/; 也可以直接透過[Google Play 軟體商店](https://play.google.com/store/apps/details?id=org.thoughtcrime.redphone)[下載](https://whispersystems.org/)  
**系統需求:** Android 2.2 以上版本  
**本指南使用版本:** RedPhone 0.9.6  
**版權宣告:**免費開源軟體 ; GPLv3  
**程度:** 初學者-中級  
**其它參考資料:** [http://support.whispersystems.org/](http://support.whispersystems.org/)  
**所需時間:** 15分鐘  
**使用RedPhone 能讓你:**  
在無線網路或資料傳輸時用你一般的電話號碼來撥打加密語音電話  
注意: RedPhone 只能在雙方皆安裝使用RedPhone或是 Signal (iPhones用)軟體的情況下才能進行加密功能. ([後者請見「Signal工具指南 T](umbrella://lesson/signal)[ 來了解其在 iPhones上如何操作)](https://whispersystems.org/)  
  
**1.0 如何安裝RedPhone**  
**第 1步:** 下載與安裝RedPhone  
在你的Android手機上, 進入Google Play 商店應用程式並尋找"RedPhone:: Secure Calls."  
選擇安裝前得先同意其服務條款，然後此應用程式將會自動下載與安裝到手機上.![](http://self.jxtsai.info/tool_redphone1.png)  
**第2步:** 註冊你的手機號碼  
一旦安裝好後，請啟動它，你將會被自動引導要求註冊你的手機號碼.![](http://self.jxtsai.info/tool_redphone2.png)  
完成註冊手機門號後, RedPhone會傳送一則 SMS 簡訊到你的手機上以確認該組門號的確為你所有.則這個認證碼輸入到應用軟體後，你就順利地完成了 RedPhone 安裝並能夠透過它來撥打加密的電話!  
  
**2.0 使用RedPhone**  
為了能使用 RedPhone, 你所欲通話的對象也要安裝好 RedPhone (或 Signal). 如果你試著利用RedPhone 撥打電話給某人但他們還沒安裝過這個軟體,這時此應用程式會詢問你是否要主動透過SMS簡訊邀請對方也使用RedPhone,否則它不能讓你透過這個軟體來完成打電話動作.![](http://self.jxtsai.info/tool_redphone3.png)  
當你撥打電話給其它的RedPhone 或 Signal使用者時 (不管是從一般的手機撥話系統還是透過軟體), 你將會被給予一組隨機的對照文字.這個文字對比組合讓你可以來確認你的身分以及其它使用者的密鑰，也就是一般所知的密鑰認證方式.![](http://self.jxtsai.info/tool_redphone4.png)  
最可靠的通話者認證方法是透過頻外授權out-of-band authentication來比對文字. 如果你認得出對方的聲音，也可以大聲地念出你被分配到文字組合來比對確認,但厲害的攻擊者也許能夠竊聽到而進行破壞 . 比對的文字必須要一模一樣才行.

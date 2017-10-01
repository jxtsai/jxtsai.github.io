---
author: jx tsai
comments: true
date: 2016-05-18 09:33:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/05/18/textsecure-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97/
slug: textsecure-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97
title: TextSecure 工具指南
wordpress_id: 76
categories:
- android
- localization
- opensources
- Security First
- umbrella app
---

[Security First’s umbrella app](https://secfirst.org/)的正體中文化初稿系列資料。TextSecure據說是比whatsapp/telegram 更為安全的手機傳訊軟體,我[去年也曾簡單介紹過](http://self.jxtsai.info/2015/03/blog-post_5.html)。至於台灣長官們愛用的line，真是受夠了,當然痛快地成為它的拒絕往來戶。  
  
***本文為Security First製作的手機應用umbrella app正體中文化翻譯系列資料之一。目前仍為初稿狀態，虛心接受指正批評。原始的json資料格式配合app電子書的html編輯標籤，轉貼到部落格上排版混亂也欠缺原始圖檔請見諒。***  
  
**TextSecure 工具指南**--Android手機上的安全簡訊軟體  
![TextSecure](https://2.bp.blogspot.com/-KDiQvTj5r0M/V35CCnLLr9I/AAAAAAAAKVE/mDVQoWARtLQm2DAJ90wVBXVl-tYLjVZRQCLcB/s1600/imagen-textsecure-beta-1ori.jpg)  
**學習內容:[傳送簡訊](umbrella://lesson/sending-a-message)  
**下載點:** TextSecure可自 [Open Whisper Systems](https://whispersystems.org/)官網下載;也可以透過[Google Play 商店](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)來取得**  
**系統需求:** Android 2.3 以上版本  
**本指南使用版本:** TextSecure 2.1.7  
**版權宣告:** GPLv3  
**程度:** 初學者 - 中級  
**其它參考資料: **  
[https://github.com/WhisperSystems/TextSecure/wiki/Using-TextSecure](https://github.com/WhisperSystems/TextSecure/wiki/Using-TextSecure)  
[https://securityinabox.org/en/textsecure_main](https://securityinabox.org/en/textsecure_main)  
[http://support.whispersystems.org/](http://support.whispersystems.org/)  
**所需時間:** 15分鐘  
**使用TextSecure 能讓你:**透過手機傳送私密的端對端加密簡訊  
  
**1.0 開始之前**  
注意: TextSecure必須有無線網路或是電信上網來進行. 如果沒有網路連線，目前的版本仍可以用於傳送SMS簡訊 , **但基於安全考量，這個功能將在未來的更新版本上被取消而只能透過連網來傳送訊息路.**藍色的訊息是透過資料傳輸而綠色訊息則是由SMS傳送.TextSecure目前也可以用於傳送SMS簡訊給非TextSecure 用戶,但這些訊息傳送時並未經過加密.有加密的訊息會顯示出一個小鎖的標記.雙方都必須使用TextSecure 透過網路安全傳送加密訊息.  
你可以設定一串密語來加密手機上儲存的通訊對話內容. 萬一你的手機遭到没收或是損害，這些資料仍然受到較安全的保護.TextSecure 支援30種以上語言版本. 你可以透過在「設定」“Settings”選單下的 「語言」"Language"選項來變更語言包.  
  
**2.0如何安裝TextSecure**  
**第1步:**下載和安裝TextSecure:在Android 手機上, 進入Google Play 商店找尋"TextSecure".選擇”TextSecure Private Messenger“應用軟體.  
選擇安裝並同意接受其服務條款後，應用軟體將會開始自動下載與進行安裝.![](http://self.jxtsai.info/tool_textsecure1.png)  
**第2步:** 創建一組密語以用來加密手機上的資料  
打開應用軟體後. 你將會被要求創建一組密語以用來加密手機資料. 這表示你的資料在傳送過程中已受到加密保護, 而在自己手機上的訊息也同樣被加密. 如果你跳過了這個步驟, 你的訊息仍然會在傳送之前被加密, 並未沒有在手機上加密保護. 要了解這方面更多的資訊請參考**[密碼課程](umbrella://lesson/passwords).![](http://self.jxtsai.info/tool_textsecure2.png)  
**第3步(可選):**滙入現有的文字簡訊**  
你會被問道是否要將手機上已有的文字簡訊滙入到TextSecure的加密資料庫中. 這端視你個人的需求: 它可以把舊有的文字簡訊(SMS) 滙入到TextSecure 應用軟體中並予加密.  
**第4步(可選):** 用手機門綁定號註TextSecure  
下一步會詢問你是否要把手機門號綁定在TextSecure的連線註冊. 若其它的使用者也用TextSecure 這可以省下傳SMS簡訊的電信費用. 這是可選的非必要步驟.一旦你登記了你的手機門號, TextSecure 會自動傳送一則認證簡訊到你的手機上.  
  
**3.0 認證密鑰**  
TextSecure 使用端對端的加密.當你首次透過TextSecure傳訊簡訊給另一位也是使用TextSecure的用戶，這個應用軟體會啟動一組密鑰交換訊息給雙方.你必須用這個密鑰來和對方進行確認步驟, 這部份可參考電子前哨基金會EFF有關[Key Verification密鑰認證](https://ssd.eff.org/en/node/37/)的介紹).  
點選螢幕右上方的小掛鎖圖示後選擇其中的「認證密鑰」”Verify Identity“，你將可以看到二組密鑰，一個是你自己的一個是對方的.TextSecure 支援條紋碼掃描或手動認證方式. 如果通訊雙方正好在同一處空間，你們可以透過手機上的條紋認證碼掃描(其位於對話視窗上方的選單，選擇「認證身份」“verify identity”選項然後點擊絛紋碼圖示)或是大聲念出彼此的密鑰碼內容給對方比認.但如果你們不在同一個空間, 還是有其它可以嘗試的方法來確認密鑰內容.例如說 For example, 如果認得出對方的聲音，可以透過語音電話來讀出密鑰內容，或是利用其它的已確認安全的通訊管道如 PGP or OTR來傳送密鑰內容.

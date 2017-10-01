---
author: jx tsai
comments: true
date: 2016-05-15 11:17:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/05/15/%e5%ae%89%e5%8d%93%e6%89%8b%e6%a9%9fandroid%e7%9a%84%e5%9f%ba%e6%9c%ac%e5%ae%89%e5%85%a8%e8%a8%ad%e5%ae%9a%e6%8c%87%e5%8d%97/
slug: '%e5%ae%89%e5%8d%93%e6%89%8b%e6%a9%9fandroid%e7%9a%84%e5%9f%ba%e6%9c%ac%e5%ae%89%e5%85%a8%e8%a8%ad%e5%ae%9a%e6%8c%87%e5%8d%97'
title: 安卓手機Android的基本安全設定指南
wordpress_id: 79
categories:
- android
- localization
- opensources
- Security First
- umbrella app
---

依舊是[Security First](https://secfirst.org/index.html)'s umbrella app 的正體中文資料。  
  
據說過去十年是智慧型手機風光成長的黃金時代,但所謂的「過去」也意指了一個不再復返的美好歲月。雖說老老少少都使用智慧型手機過著幸福快樂的日子（？），但佔了智慧型手機市佔百分之九十的安卓手機Android系統使用者，恐怕絕大部份都不知道其基本的安全設定吧。三四年前，在某一個半公開的演講場合中，介紹數位資案的講者詢問聽眾在場有誰有做了手機加密？當下我還以為所謂的加密不過就是把手機載上螢幕鎖/PIN設定的保護功能。自以為資安意識高於常人者如我，竟不知道手機加密這回事(或者更準確地說，不知道資料加密和密碼設定**完。全。是。兩。回。事。**)，那麼恐怕百分之九十九的安卓手機使用者更沒聽說過吧。在作umbrella app中文化的過程中，有關智慧型手機的一些基本常識令我受益不少，故這系列翻譯初稿也會包括基本的手機安全等介紹。  
  
***本文為Security First製作的手機應用umbrella app正體中文化翻譯系列資料之一。目前仍為初稿狀態，虛心接受指正批評。原始的json資料格式配合app電子書的html編輯標籤，轉貼到部落格上排版混亂也欠缺原始圖檔請見諒。***  
  
安卓手機的基本安全設定指南![Security Android](https://3.bp.blogspot.com/-SAEkL_bW-54/V35EPP_b4iI/AAAAAAAAKVY/Q88cCVrE5Ogk_C6_m0011-sDf4eztay-wCLcB/s1600/Basic-Android-Security.png)（圖片偷自：http://firmwareandroidyes.blogspot.tw/2015/11/basic-android-security-setup-guide.html）  
  
**學習內容: [行動電話](umbrella://lesson/mobile-phones)  
**手機系統需求:** Android 4.4  
**程度:** 初學者  
**所需時間:** 5分鐘**  
  
**1.0 基本設定  
1.1 取得手機權限**  
在「設定」Settings -> 「個人」Personal ->「安全」 Security -> 「設定」Set up下找到「SIM 鎖」選項SIM card lock **啟動** _「鎖住SIM卡」Lock SIM card_. 這樣你每次打開電話時，必須輸入其PIN號碼才能解鎖,沒有正確的PIN 就無使用電話.  
**而要設定** _螢幕鎖_,則到_「設定」Settings -> 「個人」Personal -> 「安全」Security -> 「螢幕鎖」Screen Lock_, 然後它會要求輸入設定一組簡碼、模式或密碼來執行螢幕解鎖. 我們建議使用PIN 或密碼 Password選項,因為這兩者不會限制長度.你可在[「密碼課程」](umbrella://lesson/passwords)找到更多關於創建高強度密碼的資訊.  
**設定**_安全鎖計時_, 將在過一定時間後自動將手機鎖上. 你可以決定多長時間較符合你的需求習慣，這也視你是否願意常常解鎖手機而定.  
  
**1.2 手機設備加密**  
如果你使用的是Android 4.0以上的版本, 你應該 **啟動** _設備加密選項_. 這功能位於_「設定」Settings ->「個人」 Personal ->「安全」 Security ->「加密」 Encryption_.在你進行手機加密前, 你得先要設定好螢幕鎖(請參見前述).  
**注意:** 進行手機加密前,確認手機電池時間或是接上電源線.  
  
**1.3 網路設定**  
把無線網路與藍牙調整成**預設關閉**狀態. 確認無線與網路設定下的 _「網路共享」Tethering_ 與_「行動熱點」Portable Hotspots_的功能在無須使用時關閉. 其設定位於_「設定」Settings -> 「無線與網路」Wireless & Networks -> 「更多」More -> 「網路共享與行動熱點」Tethering & Mobile hotspot_  
如果你的手機支援_近場通訊(NFC)_,一般原廠多預設為開啟，請務必記得手動將其改設為關閉 .  
  
**1.4 定位設定**  
**關閉** _無線網路_ 與_GPS_ 定位 (其在 _「定位服務」Location Services_) 和手機資料(位於 _「設定」Settings ->「私人」 Personal ->「位置」 Location_).  
**注意:** 只在需要時才啟動定位功能. 最好不要讓它預設為開啟狀態，以降低位置被追踪的風險、節省手機電力、減少應用程式在背後或是電信業者遠端傳送不必要的資料.  
  
**1.5 來電顯示**  
如果你想隱藏自己的來電顯示,可到_「手機撥號」Phone Dialler ->「設定」settings -> 「其它設定」Additional Settings -> 「來電顯示」Caller ID ->「隱藏號碼」 hide number_.  
  
**1.6 軟體更新**  
要確保手機安全最好能保持軟體是最新狀態. 有二類更新方法可以檢查  
  
手機作業系統: 請到 : _「設定」settings ->「關於手機」 About phone -> 「更新」updates ->來檢查是否要更新_  
手機上安裝的應用程式：開啟 **「應用程式商店」Play store** , 從其_邊欄選單中_點選 **「我的應用程式集」My Apps**.**注意:** 當要進行軟體更新時，最好從一個可信任的網路連線(如自家)進行而不是在網咖或咖啡店.

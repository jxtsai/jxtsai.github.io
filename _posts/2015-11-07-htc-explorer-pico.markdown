---
author: jx tsai
comments: true
date: 2015-11-07 14:51:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2015/11/07/htc-explorerpico-%e5%ae%89%e8%a3%9d-cyanogenmod-10/
slug: htc-explorerpico-%e5%ae%89%e8%a3%9d-cyanogenmod-10
title: hTC explorer(pico) 安裝 cyanogenmod 10
wordpress_id: 115
categories:
- android
- CyanogenMod
---

用了兩年半的小米2S手機這週再次不慎掉落地上，導致觸控螢幕左上角出現一小處的碎裂以及一條細痕，這一摔讓螢幕左上角一小處觸控出現了無法感應的情況但當下也沒多注意，不過幾天後，不但短短細痕越變越長，觸控感應的失靈也從邊角的一小處漫延到中心大部份，這時候整個營螢幕往往無法回應觸控後的指令，畫面也會出現整個app 不停抖動的情況。看來解決方式只有二個：再次[送修螢幕換新零件](http://self.jxtsai.info/2015/11/htc-explorerpico-cyanogenmod-10.html)就是新換一支手機，但二者的經濟成本對此時的我似乎都有點過高，於是得再另思其它方法來應付我目前的需求。  
  
仔細評估，其實自己現下也沒必要用手機做什麼人情交流工作處理，智慧型手機於我而這就是：閱讀tweets, RSS, email，PTT，反正自己還有另一台[平版電腦](http://self.jxtsai.info/2014/11/htc-explorer.html), 足以應付以上需求，那麼顯然我只需要一支智障型手機來處理極輕度的接打電話工作即可。查一下，目前市面上的非智慧型手機其實也不便宜啊'.^||，那就再回來看看手邊其它退役的手機是否能接手這個只要接電話打電話的任務（咦，這不是手機原來就該有的功能嗎）。  
  
手邊還有二台智慧型手機，一是中國GMATE6577的孤兒手機，但電池早已老化無法開機；另一台則是只用來作慢跑時運動軌跡記錄的[hTC explorer](http://self.jxtsai.info/2014/11/htc-explorer.html)。幫後者裝sim card 後才發現自己當初在刷機時，連手機的打電話功能都給它刪除掉了'_'|||，呃，那乾脆一不作二不休先拿它試著安裝cyanogenmod 好了。  
  
所謂[caynogenmod](https://zh.wikipedia.org/wiki/CyanogenMod)，是基源於android的開源手機作業系統，排除了手機製造商硬加入的鎖機、間諜後門、捆綁軟件限制，讓使用者有更大的彈性與隱私安全保護來使用智慧型手機。更酷的是，有一些老機子原廠已不再支援作業系統更新了，但cyanogenmod卻可以突破這些窘境，讓老機回春。以我打算來實驗的hTC explorer 為例，這支2011年上市的手機使用的是android 2.3，無法升級到更新的版本，但是在安裝cyanogenmod時，各家熱心高手開發的更新版本，卻可以讓我一口氣把這支又舊又低階的手機昇級到[cyanogenmod 11](http://forum.xda-developers.com/showthread.php?t=2535682), 等同於android 4.4 版本。（不過我沒選擇這一版，畢竟只想用來接打電話和運動軌跡記錄器,故只用了應該是基於android 4.3 版本開發的10.2版穩定版）  
  
我的刷機過程簡單記錄如下:  
  
1. 下載符合自己手機機型所預安裝的 cyanogenmod 版本（CyanogenMod 官網上有各家手機正式認可版本或非正式認可的ＲＯＭ可供下載，XDA論壇也累積了許多高手提供的資源), 然後將其壓縮檔存放在手機的mini sd card 上  
  
2. 關悼手機電源, 以recovery 模式開啟(關機狀態下長按"電源"與"音量下"二鍵)，即會出現黑色選單的畫面，這時可用上下音量鍵來選擇所欲執行之功能，按電源鍵即為確定執行。  
  
3. 在recovery 選單下,先選擇 wipe data / wipe cache 執行這兩道手續。  
  
![](http://rootmyandroid.org/wp-content/uploads/2013/10/install-cwm-on-htc-explorer-300x253.png)  
  
4. 完成 wipe 之後,仍然在recovery 選單下,選擇" install zip from sdcard", 然後選擇己存入SD card 的cyanogenmod 壓縮檔。這時手機應該就自動在進行安裝，等再次出現recovery 選單畫面後，只要再次選擇reboot 重新開機。  
  
5. 手機重開機後,就會發現這時手機的歡迎畫面成了cyanogenmod　logo,第一次載入可能時間會稍長一點,完成後系統就會要求使用者進行一些語系選取，要不要註冊cyanogenmod帳號等簡單的設定詢問，其實沒註冊綁定任何帳戶還是可以好好使用cyanogenmod，不像在google 的管轄下，多會要求用戶綁定一個gmail或google app 帳號才能從google play 下載東西。（因為手機的畫面截取功能失靈，故無法上傳畫面給大家看）  
  
6. 只打算拿來接打電話,所以我連google apps都沒安裝 XD，另外再從SD card 順利安裝啟動endomondo apk　作為慢跑時的運動記錄計時器。   
  
7. 這支手機之前就曾經越獄解鎖取得root權限,所以已安裝了recovery 模式，故不贅述此一步驟(其實當時沒記，現在也忘了是怎麼做到的)

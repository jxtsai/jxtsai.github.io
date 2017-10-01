---
author: jx tsai
comments: true
date: 2016-08-03 03:41:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/08/03/rocketchat-%e7%84%a1%e7%97%9b%e5%ae%89%e8%a3%9d/
slug: rocketchat-%e7%84%a1%e7%97%9b%e5%ae%89%e8%a3%9d
title: RocketChat 無痛安裝
wordpress_id: 37
categories:
- javascript
- opensources
---

![](https://4.bp.blogspot.com/-iulfCgg8CYM/V6G-wtKbW5I/AAAAAAAAKs4/_udYaidaAgcr8Bg8TBSfM1inVt-sMo27gCLcB/s1600/RocketChat.jpg)  
最近因為在查[MatterMost](https://mattermost.org/)的安裝佈署方式，找到一篇[介紹替代Slack 開源團隊溝通軟體的介紹文](https://blog.okturtles.com/2015/11/five-open-source-slack-alternatives/)，RocketChat即是五款之一。其官網上的ubuntu安裝介紹看起來說難不難，因之前完全沒用過MongoDB，所以看到它的設定部份，心理似乎有著先入陌生的恐懼障礙。但在RocketChat開出來的一大串可供安裝部置的方式中，嚇然發現也有清楚寫明如何安裝在nitrous平台（近來常利用它的免費服務來玩些有的沒有）的介紹,而且看起來蠻簡單的，立馬決定一試。  
  
依Rocket.Chat官網文件的說明，可以利用nitrous.io其quickstart,建立一個“Meteor box”來安裝。但奇怪的是，我在nitrous.io首頁底下雖然找到quickstart的連結，但點選打開之後，卻一直無法出現如Rocket.Chat所描述的畫面。  
![](https://1.bp.blogspot.com/-nYkUyERH8EQ/V6DDQB1bRMI/AAAAAAAAKrA/TTrY_Fh1yaAHWEmD5On2E8btHLNxXzfVgCLcB/s1600/Screenshot%2Bfrom%2B2016-08-02%2B23%253A58%253A39.png)  
![](https://1.bp.blogspot.com/-WPlEwOE1OOo/V6FbXa62lwI/AAAAAAAAKso/WqX8FapZYEEPDz0gXEUYC_pP7IAYRanjwCLcB/s1600/quick.png)   
  
於是轉到Rocket.Chat在儲放其程式碼代管服務的github.com專案說明首頁readme，才發現其中已建立了一個在nitrous.io上佈署建置的連結按鈕（也包括其它許多提供類似服務網站的快速部署按鈕，如Heroku，windows azure等等）。於是我輕鬆一按這裏的[nitrous.io quickstart按鈕](https://github.com/RocketChat/Rocket.Chat),馬上開啟一個新分頁，顯示nitrous.io正在為我建立一個Rocket.Chat的專案。  
![](https://2.bp.blogspot.com/-w-tW86tfL3s/V6DKeOAtfWI/AAAAAAAAKr8/3KfbQ_h_xhcOvbVi2YeprTIAMy9IwkSNQCLcB/s1600/quickstart.png)  
  
過了3~5分鐘之後，一個佈署在nitrous.io的Rocket.Chat專案環境已準備妥當必要依賴的支援套件、資料庫軟體等等都已一應俱全，用戶可以進入到開發環境底下。  
![](https://2.bp.blogspot.com/-QhHR2DJ5JFE/V6DHNLSfHHI/AAAAAAAAKrc/Dm0qiEOWecYJArw6jrbw05lwfTW3puVZgCLcB/s1600/nitrous.png)  
  
接下來就利用開發環境的文字指令區，依Rocket.Chat文件說明，把工作目錄切換到 /Rocket.Chat/底下（可參考IDE環境的左上方專案目錄樹狀結構找出正確的切換路徑）。  
要啟動Rocket.Chat，只要在 Rocket.Chat/目錄下，打入 meteor 指令，其就會自動下載安裝Rocket.Chat以及其相關套件，過程約2~3分鐘吧。  
![](https://1.bp.blogspot.com/-Lvn_FDj-xPM/V6DMj3A_xnI/AAAAAAAAKsM/9vhK-mIlYwQ1lmT7Z0j_5bO4NILwsIDwgCLcB/s1600/lauch.png)  
![](https://4.bp.blogspot.com/-dl9x9SSSxlw/V6DNnouVjnI/AAAAAAAAKsY/iOEyKAkmBFUe8tB57oNMAFTddb8l1_YAACLcB/s1600/success.png)  
當console出現如上圖 => App running at : http://localhost:3000/ 的訊息畫面時，就表示已完成安裝，這時候選擇上方功能列 Preview選項最上方第一個選項：Port 3000，瀏覧器就會打開專案的網址。鐺鐺鐺鐺，Rocket.Chat已經成功安裝好了。  
![](https://1.bp.blogspot.com/-IZ-_Lhork2g/V6DJR4LSheI/AAAAAAAAKro/6X0vknbt2r8iSJSk2GtbD_ST0vorHkBBACLcB/s1600/Screenshot%2Bfrom%2B2016-08-02%2B23%253A51%253A58.png)  
  
這是Rocket.Chat註冊登入後的使用者介面  
![](https://2.bp.blogspot.com/-rTvNlpMnOTU/V6DJrEHsg0I/AAAAAAAAKrs/6vcfQPQsb7A9IavzYQCk16KSLJbdHaMkACLcB/s1600/rocket.png)  
  
因為是使用nitrous.io免費版的帳號，光裝一個Rocket.Chat，就快把資源吃光了。  
![](https://2.bp.blogspot.com/-0NtzEYiTlB0/V6DJ9yzna6I/AAAAAAAAKr0/K3N9T4X-SKklG0YcRgLv8-uZTPinPBMPQCLcB/s1600/env.png)  
  
這麼神奇地讓我這個幾無寫程式碼能力的生手都可以輕易簡單地安裝好RockerChat,這個叫作meteor東西引起我進一步的好奇。查了一下資料，它是一個基於 javascript/ nodejs所撰寫的網頁應用開發框架。換句話說，以javascript來貫穿了網站前端（使用者看到體驗的內容）以及後端伺服器（nodejs）的整合開發，甚致是移動設備上的應用程式。因為目前找到有關Meteor.js新手教程的資料不多，這篇「[Meteor.js 简介](http://zhezhang.co/2015/03/introduction-meteor-js/)」則是談及了其幾個重要的特點，該篇文章最後整理了一些Meteor社群資源，包括這本Discover Meteor [的簡體中文版電子書](http://zh.discovermeteor.com/)  
  
從這次無痛快速安裝好Rocket.Chat的經驗，其前端是利用blaze 來建立使用者界面（傳統方式是當用戶端向伺服器進行一個動作請求的指令後，伺服器才會根據其指令讀取資料庫，再把回應資料送回到用戶端。但在其響應式即時特性則是每當資料數據改變時，用戶端頁面就會及時同步自動更新，而不需進行請求），以Meteor開發框架作跨平台應用的整合開發與使用，從其安裝部署上就可以體會到Meteor的強大。從這個過程中反而我下定決心：決。不。要。花。時。間。去學習某一個特定的網頁開發框架，因為程式軟體世界的變化速度實在太快太多了，時不時一兩年內又會出現另一個驚動江湖的高手引領派別招式風騷，不多久又是一山又比一山高的風華漸去。我只想要偶而被浪頭打到地稍稍體會感受一下某個風潮之所以為何能形成之魅力，一如這樣胡亂地動手試作著各開源軟體的安裝部署就好。  


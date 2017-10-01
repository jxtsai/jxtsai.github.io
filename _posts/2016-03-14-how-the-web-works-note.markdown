---
author: jx tsai
comments: true
date: 2016-03-14 15:42:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/03/14/how-the-web-works-%e5%b0%8f%e7%ad%86%e8%a8%98/
slug: how-the-web-works-%e5%b0%8f%e7%ad%86%e8%a8%98
title: How the Web Works 小筆記
wordpress_id: 90
categories:
- coding
- dotlife
- reading /watching/ listening
---

從[Free Code Camp](https://medium.freecodecamp.com/) (提供NPO的網路開源工具與實用文件)整理在Medium (號稱是第三代部落格的個人線上出版平台)，讀到由正妹[Preethi Kasireddy](https://medium.com/@preethikasireddy) 寫的系列文章。她自述自身教育背景為財務管理非而正式學院電腦資訊科班訓練，也曾在舊金山矽谷的科技資金創投工作過一段時間後，決定離職投入自學的程式開發撰寫的工作。我讀了她的幾篇文章，可以感受到作者做為一個半路出家的程式開發（學習）者，自覺更有責任扮演完全剛入門新手與開發大師之間的溝通角色。她的文章一再試用著最簡單的語言來解釋一些老手之間早已視為理所當然但新手卻摸不著頭緒的觀念與原理。例如這一系列「How the Web Works」的閱讀，讓我重溫掌握最基本知識之必要，也透過文字行間提及整理的概念，鋪陳某些程式開發上重要的共同規則，一解我曾經在閱讀相關文章時的疑惑，故以此文作一點筆記。  
  
Part I: [How the Web Works: A Primer for Newcomers to Web Development](https://medium.freecodecamp.com/how-the-web-works-a-primer-for-newcomers-to-web-development-or-anyone-really-b4584e63585c#.mxclusyah) (or anyone, really)  
從最基本的術語拆解，說明網際網路（互聯網）中的全球資訊網(world wide wed)到底是如何運作。  
  
Part II : [How the Web Works Part II: Client-Server Model & the Structure of a Web Application](https://medium.freecodecamp.com/how-the-web-works-part-ii-client-server-model-the-structure-of-a-web-application-735b4b6d76e3#.png8ad8m3)  
解釋最基本的網頁連線架構，包括用戶與伺服器主機如何溝通、網頁應用程式架構，也稍提及中應用程式裏面的程式演算法應用來處理各類請求與功能回應效率提昇（參見下圖）、使用CDN（Content Delivery Networks）代理服務提昇讀取速度。  
![](https://d262ilb51hltx0.cloudfront.net/max/800/0*zFuBGTUicpKAES3J.png)  
  
Part III : [How the Web Works Part III: HTTP & REST](https://medium.freecodecamp.com/how-the-web-works-part-iii-http-rest-e61bc50fa0a#.5nb3tcmv9)  
進一步說明HTTP,也就是用戶端與伺服器之間的溝通協議如何進行。在這裏作者也稍微解釋了什麼是「REST（ful）」 for application (REST stands for "Representational State Transfer")。之前曾在雲端運算的某處讀過「stateless」（姑譯之為“無狀態”），根本丈二金剛不知道指的是什麼。幸而在這篇文章中，作者作了簡單的說明，讓我才有點能夠想像所謂地追求「無狀態」這回事與應用程式、大量資料處理、機器效能之間的關係。  
  
Part IV: Code examples of client-server interactions （最後一文似乎暫未寫好？）

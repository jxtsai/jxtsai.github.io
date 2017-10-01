---
author: jx tsai
comments: true
date: 2016-08-18 00:56:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/08/18/school-of-data-5-%e6%95%b8%e6%93%9a%e6%96%b0%e8%81%9e/
slug: school-of-data-5-%e6%95%b8%e6%93%9a%e6%96%b0%e8%81%9e
title: School of Data -5 數據新聞
wordpress_id: 28
categories:
- DataAnalysis
- journalism
---

之前陸續整理了自學School of Data 關於認識數據入門的線上教材的記錄、心得和感想，（[School of Data -1 數據資料入門20160714](http://self.jxtsai.info/2016/07/school-of-data-1.html); [School of Data -2 數據清理入門0160717](http://self.jxtsai.info/2016/07/schoo-of-data-2.html); [School of Data -3 數據探索之道20160721](http://self.jxtsai.info/2016/07/school-of-data-3.html); [School of Data -4 從網路上抓取數據20160809](http://self.jxtsai.info/2016/08/school-of-data-4.html)）。本文應該是這一系列School of Data的最後一篇「稍有」系統化的整理，接下來可能暫時去忙的東西，如果有機會學到中階進級程度的數據學習材料再視情況來整理吧。  
  
按School of Data網站上的順序，原來接下應是介紹地理標記資料（Mapping）、預算支出數據（Budgets and Spending Data），以及如何利用手機來收集數據等學習。不過前二門課，我看了一次內容，還不能理解與吸收如何使用地理數據資料，對於國家公部門歲出歲入的財政數據，也還不太熟悉，得再花上一點時間來摸清，故等我弄清楚了，再來為文整理。至於如何使用手機來收集收據，過去曾經上過TechChange 的線上課程，自我感覺良好地以為算是有一些基本概念，且評估這門課對我個人實際用處不大，故先搞定其它東西再說。  
  
根據SOD原本在數據新聞一課中所放入的相關單元應包括：  
A) <strike>Getting Stories from Data</strike>   
B) Using TimemapperJs for data storytelling  
C) <strike>Asking for Data</strike>   
D) <strike>Spending Stories</strike>   
E) <strike>Making Data pretty</strike>  
但這五個單元除了第二個利用javascript寫成的程式（TimelineJS; TimemapperJS）可整合時間軸與google map/ openstreet map作為故事/新聞事件在地理標記上的呈現外，其它四個單元的內容連結早已失效。從各單元的標題介紹猜想，A)Using TimemapperJs for data storytelling，這章應該與SOD:A Gentle Introduction to Mapping重疊性高；C) Asking for Data則為Data Fundamentals之中的第二個單元：Finding Data； D)Spending Stories則為“Working with Budgets and Spending Data”的應用篇；而最後一個單元E)Making Data pretty則是進行視覺化的設計呈現産出。找遍SOD網站，似乎數據資料分析能與新聞報導直接掛上關係的教材資源，就是2011年MOZfest活動中，由一群新聞工作者發起的手冊撰寫協作計畫，而稍後英國OK Foundation 也加入贊助此專案，在半年後完成了第一版的「The data journalism handbook」 一書。  
  
既然SOD網站上找不到原本「數據新聞」課程的相關單元材料，就只好翻讀上面提到的這本[The data journalism handbook](http://datajournalismhandbook.org/1.0/en/)，作為了解「數據與新聞」入間教材吧。讀著該書第一章引言介紹，某種似曾相識之感才想起這本書其實我在去年初已曾經翻讀過，還寫下了一篇沒什麼內容的筆記（[data journalism 20150131](http://self.jxtsai.info/2015/01/data-journalism.html)，嗯有些寫過的東西做過的事講過的話，果然一段時間後回過頭來看，真叫自己羞瘣,但後兩者，事情和話語相較下更難以留下記錄吧）。當初看得似乎被某些名門大戶（New York Times, Guardian）專業新聞團隊弄得很眩的數位呈現所迷惑，如今再重新來讀讀應該另有一番不同的感受吧。抓出了該書的編寫章節架構如下：  
  


[![](https://3.bp.blogspot.com/-HRoXjgbcbUA/V5gYS0-AmXI/AAAAAAAAKl0/Tyw2hEVhtjQsXFXUrGsWTX75Xu4PBv71ACLcB/s1600/cover_print.png)](https://3.bp.blogspot.com/-HRoXjgbcbUA/V5gYS0-AmXI/AAAAAAAAKl0/Tyw2hEVhtjQsXFXUrGsWTX75Xu4PBv71ACLcB/s1600/cover_print.png)

  
A）Introduction  


  * What Is Data Journalism?
  * Why Journalists Should Use Data
  * Why Is Data Journalism Important?
  * Some Favorite Examples
  * Data Journalism in Perspective
  
B）In The Newsroom  


  * The ABC’s Data Journalism Play
  * Data Journalism at the BBC
  * How the News Apps Team at Chicago Tribune Works
  * Behind the Scenes at the Guardian Datablog
  * Data Journalism at the Zeit Online
  * How to Hire a Hacker
  * Harnessing External Expertise Through Hackthons
  * Following the Money: Cross-Border Collaboration
  * Our Stories Come As Code
  * Kaas & Mulvad: Semi-finished Content for Stakeholder Groups
  * Business Models for Data Journalism
  
C）Case studies  


  * The Opportunity Gap
  * A 9 Month Investigation into European Structural Funds
  * The Eurozone Meltdown
  * Covering the Public Purse with OpenSpending.org
  * Finnish Parliamentary Elections and Campaign Funding
  * Electoral Hack in Realtime
  * Data in the News: Wikileaks
  * Mapa76 Hackathon
  * The Guardian Datablog’s Coverage of the UK Riots
  * Illinois School Report Cards
  * Hospital Billing
  * Care Home Crisis
  * The Tell-All Telephone
  * Which Car Model? MOT Failure Rates
  * Bus Subsidies in Argentina
  * Citizen Data Reporters
  * The Big Board for Election Results
  * Crowdsourcing the Price of Water
  
D)Getting Data  


  * A Five Minute Field Guide
  * Your Right to Data
  * Wobbing Works. Use it!
  * Getting Data from the Web
  * The Web as a Data Source
  * Crowdsourcing Data at the Guardian Datablog
  * How the Datablog Used Crowdsourcing to Cover Olympic Ticketing
  * Using and Sharing Data: the Black Letter, Fine Print, and Reality
  
E)Understanding data  


  * Become Data Literate in 3 Simple Steps
  * Tips for Working with Numbers in the News
  * Basic Steps in Working with Data
  * The £32 Loaf of Bread
  * Start With the Data, Finish With a Story
  * Data Stories
  * Data Journalists Discuss Their Tools of Choice
  * Using Data Visualization to Find Insights in Data
  
F)Delivering Data  


  * Presenting Data to the Public
  * How to Build a News App
  * News Apps at ProPublica
  * Visualization as the Workhorse of Data Journalism
  * Using visualizations to Tell Stories
  * Designing With Data
  * Different Charts Tell Different Tales
  * Data visualization DIY: Our Top Tools
  * How We Serve Data at Verdens Gang
  * Public Data Goes Social
  * Engaging People Around Your Data
如果有自學過School of Data提供的線上數據入門課程者，顯然可以輕鬆了解：D)Getting Data（對應[School of Data -1 數據資料入門](http://self.jxtsai.info/2016/07/school-of-data-1.html)）; E)Understanding data (對應[ School of Data -3 數據探索之道](http://self.jxtsai.info/2016/07/school-of-data-3.html) )的內容，而先把該書的閱讀重點放在A)Introduction與F)Delivering Data這兩章。A)的引言簡介對於非正統新聞媒體科班訓練出身的公民，算是能夠從這裏掌握到一點新聞學本身的倫理以及數據資料在新聞學應用結合的發展契機。然後利用D)E) 同步回顧複習一下 School of Data前三門數據入門課程的內容後，再來讀F)Delivering Data（可配搭配另一篇Data+Desing，了解設計視覺化産出過程中要留意的面向,請見之前的介紹：[Data+Design數據資料視覺化入門書20160728](http://self.jxtsai.info/2016/07/datadesign.html) ）。至於該書B）In The NewsroomC）Case studies，應是比較偏實戰案例的新聞室編輯台作業，若有暇時或許可以把它當作茶餘飯後入睡前的小故事來讀讀。這是我對這本「The data journalism handbook」閱讀上拆解的建議。  
  
另外[GIJN(Global Investigative Journalism Network)網站](http://gijn.org/)與推特（＠gijn）不時會介紹一些蠻實用的深度報導團隊、趨向、手法、工具。更何況它的網站還有[簡體中文版的材料](http://cn.gijn.org/)，其內容不只是對英文版故事進行中文翻譯，在本地化的過程中還加入了不少「符合中國特色」的深度報導工具與長期在工作崗位（雖然也有不少記者已被迫下崗，但仍在「記者」天職上努力不懈）上推動的新聞工作者，值得華文世界讀者按贊。其中GIJN中文編輯團隊整理了一篇「[數據新聞入門大禮包](http://cn.gijn.org/2015/04/16/%E6%95%B0%E6%8D%AE%E6%96%B0%E9%97%BB%E5%85%A5%E9%97%A8%E5%BF%85%E8%AF%BB/)」，應該也是華文社會中對於數據新聞入門最良心的建議整理吧。寫作本文時一邊查看其大禮包中提供的資源整理，才知道原來「The data journalism handbook」一書早在兩三年前已完成了[簡體中文版:数据新闻手册](http://datajournalismhandbook.org/chinese/)的翻譯與開放線上免費閱讀。  
  
再提一本“[The Curious Journalist’s Guide to Data](https://towcenter.gitbooks.io/curious-journalist-s-guide-to-data/content/)”，這是偏向從「新聞學」的角度，來討論數位時代下大數據出現後帶給新聞報導近的資料呈現趨勢，身為一名新聞工作者如何因應如此現實變化，從好奇心出發，把強化自身在數據資料親近、理解、掌握、分析等能力提昇。該書大約分為三大部份，  
A）quantification:這部份算是對新闐記者作一點對數字、數量、數據、數學恐懼的心理再建設吧？  
B）analysis:進一步透過基礎的統計學入門好讓新聞記者知道數據資料的作用與意義。   
C）communication： 這個應該是新聞記者最擅長的地方吧，如何把原本枯橾的科學研究成果或複雜的數字變成讓讀者感到相關、有意思的報導。   
  
因為我自己不太愛作者這種寫作風格（典型的記者吧，文字很多，很愛用許多陳述來介紹案例，讓我讀得很累XDXD），但如果是本身具溝通、新聞學訓練背景出身，也許對這本書採取的表現策略接受度較高吧？  
  
[learno.net](http://learno.net/)則是由EJC(European Journalism Centre)所建置的一個提供給「專業媒體工作者」的免費學習平台，其在數據學習的課程有：  
[Doing Journalism with Data: First Steps, Skills and Tools](http://learno.net/courses/doing-journalism-with-data-first-steps-skills-and-tools)[  
Managing Data Journalism Projects](http://learno.net/courses/managing-data-journalism-projects)  
[Mistakes We Made So You Don't Have To: Data Visualisation, Journalism and the Web ](http://learno.net/courses/data-visualisation-journalism-and-the-web)  
我自己並沒學習learno.net任何一門課程，無法分享其好壞評價，只是把與數據新聞相關的重要入門資源一併整理出來。  
  
  


---
author: jx tsai
comments: true
date: 2016-04-15 14:50:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/04/15/globaleaks-project-%e4%b8%ad%e6%96%87%e5%8c%96/
slug: globaleaks-project-%e4%b8%ad%e6%96%87%e5%8c%96
title: GlobaLeaks project 中文化
wordpress_id: 85
categories:
- encrypt
- human rights
- localization
- opensources
- privacy
---

最近完成了一個開源專案「GlobaLeaks」的正體中文化初步工作。開始在Ｔransifex加入GlobaLeaks正體中文化小組的契機,只是因為Open Tech Fund在上面放了４，５０個它們合作的專案，這些專案多是與網路隱私、加密通訊、言論自由、社會行動有關，我又在其中挑選了一些自己比較感興趣的專案，固定抽點時間投入協助其中文化的翻譯。  
  
[GlobaLeaks](http://logioshermes.org/home/projects-technologies/globaleaks/)是由[HERMES Center for Transparency and Digital Human Rights](http://logioshermes.org/)這個ＮＧＯ／新創社創（？）所推動的一個專案。HERMES成立的願景就是要提倡社會整體對於民主透明度與法治問責的意識與關注，因此它除了作相關主題的研究報告外，也推動某些技術性專案的開發。而GlobaLeaks就是其中一個技術性專案，希望讓媒體機構或是ＮＧＯ組織，能夠輕易地架構出一個讓吹哨者可以透過此平台進行內幕不公資訊揭露的通訊工具,讓這些體制內的不公或問題得以為外人所知。因此這種揭密平台工具的隱密與安全設計就格外重要。但說真的，我也不知道自己當初為什麼傻了心眼地以為這個東西對於台灣社會的資訊自由有所幫助，反正這裏已經有一堆粉絲人數爆長的正義魔人公社與記者們ＣＴＲＬ＋c；ＣＴＲＬ＋v的臉書動態與ＰＴＴ八卦版24小時地流竄在媒體的「即時新聞」上,而真正的吹哨者保護法令仍然遙遙無期，所謂「揭密」這回事背後的危險與故事真相也沒人要探究查證報導。  
  
![GlobaLeaks](https://1.bp.blogspot.com/-tPu8s1pSEhY/V30lmQseLoI/AAAAAAAAKRI/eXDAMwy3Ss4v-3gRTcd37xitnxPi1E0ewCLcB/s320/GlobaLeaks-1024x837.png)  
  
GlobaLeaks內容包括幾個重要成份：  
１.　GLBackend, the GlobaLeaks backend written with Python/Twisted;以Python/Twisted撰寫的後台架構。  
2. GLClient, the GlobaLeaks client written with AngularJS and Bootstrap. 由AngularJS/Bootstrap呈現的網站前端。  
另外下面兩個應是在智慧型手機使用的app開發,但目前還未對外公開  
3. GLDroid, a GlobaLeaks client for Android; this client incorporate security features such as anonymous submission with Orbot (Tor), and face anonymization with Obscuracam, thanks to the Guardian Project;  
4. iGlobaleaks-Tor, Globaleaks client for iOS.  
  
我作的正體中文化，不過是第2部份中的一段內容，我也沒有試著下載安裝到本機電腦上跑伺服器應用來體驗它的介面與功能到底如何，所以老實說，翻譯的過程很多都是只能直譯著字面上的文字，尚無法把一些簡單但關鍵的字眼好好在脈絡下詮釋出來，例如其中大量出限的"submission"一字，在GrobaLeak整個專案理念與目的上，它應該更是指（吹哨人）透過ＧlobaLeak平台工具對公共媒體進行某些資訊的揭露行動。後來在其ＩＲＣ聊天頻道上找到了一個示範的平台https://demo.globaleaks.org/, 感覺介面就像一般的wordpress 寫作與發表平台，但其中應該有進一步利用[ＧＰＧ雙重密鑰](http://self.jxtsai.info/2015/09/gpg.html)設定驗證的設計機制。

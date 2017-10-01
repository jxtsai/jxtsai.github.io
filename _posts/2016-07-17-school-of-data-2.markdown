---
author: jx tsai
comments: true
date: 2016-07-17 04:00:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/07/17/school-of-data-2-%e6%95%b8%e6%93%9a%e6%b8%85%e7%90%86%e5%85%a5%e9%96%80/
slug: school-of-data-2-%e6%95%b8%e6%93%9a%e6%b8%85%e7%90%86%e5%85%a5%e9%96%80
title: School of Data -2 數據清理入門
wordpress_id: 49
categories:
- DataAnalysis
- schoolofdata
- tactical technology collective
---

![](https://4.bp.blogspot.com/-jneFE7r0-j0/V4sB2nHSDDI/AAAAAAAAKd4/sPF6C162yXclhq5EkWNYUdvg9y9N-2DjQCLcB/s1600/schoolofdata.png)

本文為繼之前[School of Data 數據基礎入門](http://self.jxtsai.info/2016/07/school-of-data-1.html)後，再繼續整理ＳＯＤ引入Tactical Collective Technology 所編寫的「A Gentle Introduction to Data Cleaning：數據清理的友善入門」。查了一下，原來它是ＴＣＴ在２０１２年與開放知識基金會（Open Knowledge Foundation）所發展的一個課程合作計畫，ＴＣＴ協助編寫了二套數據相關課程資源,除了談數據清理的入門方法外，另一篇則是討論數據探索之道（A gentle introduction to exploring data）。為尊重ＳＯＤ與ＴＣＴ的課程安排次序，本文先介紹數據清理入門技巧，之後再來介紹第二篇數據探索的妙趣之處。以我自己讀完的感受，其實如果先介紹第二篇或許比較能夠找到樂趣與刺激學習者堅持學習的信念，因為在第一篇很容易遇上撞牆打擊初學者的信心（其實是我自己玻璃心啊XDXD）。  
  
接觸過數據處理利用者，應該都知道：數據清理是第一道非常非常非常*3重要工序，先踏實做好數據清理基本工夫，接下來才能確保處理的數據資料不會出錯，否則不管是在進一步分析的過程産生令人頭大的公式失靈、不對的計算結果，抑或最後呈現了未查覺的要命錯誤卻作公開發表等後續連鎖的倒牌效果。故數據清理的重要性自不言可喻，但它也是一個非常瑣碎又讓人頭痛的過程，我自己在摸索這一道習題過程中，就常常在公式處理上碰壁撞牆好久，根本都想放棄了。不過進入到第二階段，面對處理過完整乾淨的數據，可以在試算表或相關軟體中玩出許多有趣的東西，才會讓人發覺數據之中的妙趣故事。所以無論如何，還是得先硬著頭皮來理解一點基本的數據清理入門之術吧。  


![](https://4.bp.blogspot.com/-7Om4IyHYFVk/V4ZPPhbX81I/AAAAAAAAKc8/sdC6pmBp-4IU-1JDEwHqWuXivL8sFpcaACLcB/s1600/c09-solutions-next-gen-80-work-cleaning-data.png)

  
這門「數據清理」的課程目的是，讓學習者理解如何查察、找出試算表中不對勁的資料並加以移除以免干援影響正確公式的運算，再者學習者在這門課程後將會知道如何正確地掌握數據格式與資料類型，並將之以規則化、結構化地統一有效使用，慢慢強化自身對於收據的敏感度與洞察力。因此在學習「數據清理」之前，最好有[先上過數據基礎](http://self.jxtsai.info/2016/07/school-of-data-1.html)，掌握其基本重要知識。數據清理的友善之道主要可分成以下四大單元，而每一個單元的撰寫教學架構則是分成：a） 引言式的介紹；b)小任務練習（quick task）； c)大任務挑戰（longer task）； d)閱讀清單與參考資源補充，讓學習者可以再去探索更深入的技能知識； e) 休息與反思；此五個組成元素。  
  
前面提過，這門數據清理入門，是在Tactical Collective Technology協助下所發展出來的學習資源，一開始ＴＣＴ做出來的應該是一套工具指南：[ Using a spreadsheet to clean up a dataset](http://schoolofdata.org/handbook/recipes/cleaning-data-with-spreadsheets/)。而ＳＯＤ/ＴＣＴ為了讓學習者不至於因為原始文本過長（其實也不算太長）而感到恐懼，故又再分割成為四大單元，並以上述abcde的架構來重組、串連原本工具指南中函蓋的四大單元。  
  
1） Nuts and chewing gum：　許多時候，我們拿到的試數表，上面的數據可能是雜亂、殘缺，同一份檔案可能經過多人編輯，數據格式每個人的寫法並未統一而亂七八糟。更甚者，有些試算表也很容易被「動手腳」，刻意把某些欄列隱藏起來或是把數值資料存成文字格式所以根本無法進行計算。本單元就是讓學習者了解試算表閱讀介面的眉眉角角，並學會如何重新整理試算表格式版型編蜇排，好一步一步讓工作檔案呈現易於使用閱讀，也讓資料數據在一步一步清理的工序更為接近正確！  
  
2） the Invisible Man is in your spreadsheet, messing with your data：開啟一張試算表檔案，除了透過（李探長「眉頭一皺」）肉眼直觀式地發現許多明顯的怪異處外，其實更隱藏了許多無法一眼就認出來的錯誤待進一步細緻處理，例如儲存格中莫名的空白鍵、跨行，拼字錯誤、大小寫不同等狀況，如何透過試算表軟體的內建功能（如ＣLEAN, TRIM）來處理這類錯誤。  
TRIM(text):移除指定字串中開頭和結尾的空格  
text - 要移除的字串。  
CLEAN(text): 傳回包含無法列印且被移除的 ASCII 字元文字  
text - 將移除不可列印字元的文字內容。  
  
3） your data is a witch’s brew: 經過單元二的牛刀小試，這裏要進入學習使用試算表當中更複雜的公式與函數功能來清理試算表中不一致的數據資料。例如 ISBLANK(); LEFT(); SUBSTITUTE(); SEARCH()等函數的運用。兹將本單元中用上的函數功能作點整理：  


  * ISBLANK(value):括弧中要放入一個參數值，即為要檢查的儲存格代號，以返回該儲存格是否為空值，如果則回傳值為TRUE,否則回傳為FALSE。注意，如儲存格中內含公式，則雖然可能該儲存未顯示表面上起來未顯示任何東鈿，但ISBLANK()不會當它為空值。 
  * SUBSTITUTE(text_to_search, search_for, replace_with, occurrence_number):括弧中要放入四個參數，分別為要搜㝷對象目標、要搜㝷的內容、代換的值、發生次數。除了最後一個參數可以不放入（即默認為取代所有搜尋文字），前面三個參數都要放入。例如  


<blockquote>=SUBSTITUTE("123123123";"3";"abc") 傳回 12abc12abc12abc  
=SUBSTITUTE("123123123";"3";"abc";2) 傳回 12312abc123。</blockquote>

  * LEFT(string, number_of_characters)：傳回文字中的第一個或前幾個字元。括弧中要放入二個參數，第一個參數為「決定其初始部分字詞的文字」，第二個參數為指定起始文字的字元數，第二個參數可不放，則會默認傳回一個字元。例如

<blockquote>=LEFT("output";3) 傳回「out」</blockquote>

  * SEARCH(search_for, text_to_search, starting_at):傳回字元字串中的指定的文字段位置，第一個參數是搜㝷符合的文字段，第二個參數是搜㝷對象目標，第三個參數則表示為對第一個參數開始搜尋的位置，此參數可以不放。例如  


<blockquote>=SEARCH(54;998877665544) 傳回 10。 </blockquote>

其它試算表的函數功能，請參考：  
[Google spreadsheets function list](https://support.google.com/docs/table/25273)[  
LibreOffice Calc Functions by Category](https://help.libreoffice.org/Calc/Functions_by_Category/zh-TW#.E6.96.87.E5.AD.97)  
  
經過本單元的介紹與示範案例的動手練習後，將會更了解試算表中不同的數據資料類型，更進階高深的試算工具內建函數功能運用，如何擅用它們來檢查錯誤並清理數據。最重要的是，在這些學習清理數據的過程中，也讓初學者了解到自己在第一時間進行數據整理時，要留意檢查數據類型輸入保存的標準一致化不要犯下太多低級錯誤，方可大量減少在數據清理上要花的時間和工夫。  
  
4） 數據資料的結構化問題:到了這裏，其實正試圖把數據資料整理從試算表工具的引入使用，慢慢轉入到「資料庫」另一種結構化關聯的介紹。因為在試算表的不同欄列與各別儲存格底下，這種表現方法很難呈現某些資料其本身具有一對多面向的關係，正因為試算表這樣的据限，所以進一步學習database及其最流行的程式語言SQL，就成了繼續追㝷數據探索之道的另一個應備工具了。  
  
以上是ＳＯＤ對於數據清理的原因、基本作法、資料型態應用的介紹。除了本課程外，[ＳＯＤ網站上的資源手冊](http://schoolofdata.org/handbook)中另有一篇文章整理了[如何利用Ｏpen Ｒefine](http://schoolofdata.org/handbook/recipes/cleaning-data-with-refine/)來做數據清理的工作。Open Refine的前身是google refine，故名思義，其原本一度由google併購Freebase Gridworks底下的一個開源數據清理開源工具專案個專案，但自2012年後google 不再支援該專案，故其主力開發團隊轉而尋求社群支援，並更名為Open Refine。  
  
為考量有些數據的敏感與資訊安全，Open Refine僅提供桌面安裝版，讓使用者能在自己的電腦上處理數據清理工作，而不需上傳到遠端伺服器。它是以java 程式開發，其作業工作界面要透過瀏覧器開啟。我自己還沒有認真把它摸熟，先介紹二篇中文資料作參考：  


  * 資料視覺化網站所撰寫的圖文介紹：[史上最強大的資料整理工具 － Open Refine](http://blog.infographics.tw/2015/09/openrefine-introduction/)　
  * 全球深度報導網（Global Investigative Journalism network）的簡體中文版介紹：[数据清洗神器Open Refine简明入门](http://cn.gijn.org/2016/02/29/%E6%95%B0%E6%8D%AE%E5%88%86%E6%9E%90%E7%A5%9E%E5%99%A8open-refine%E7%AE%80%E6%98%8E%E5%85%A5%E9%97%A8/)

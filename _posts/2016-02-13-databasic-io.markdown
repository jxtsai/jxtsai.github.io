---
author: jx tsai
comments: true
date: 2016-02-13 12:16:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/02/13/databasic-io-%e8%b3%87%e6%96%99%e5%88%86%e6%9e%90%e5%85%a5%e9%96%80/
slug: databasic-io-%e8%b3%87%e6%96%99%e5%88%86%e6%9e%90%e5%85%a5%e9%96%80
title: databasic.io 資料分析入門
wordpress_id: 93
categories:
- DataAnalysis
- e-learning
- python
---

隨著技術上硬體設備強化和平價化，以及軟體開發的平易親近，數據資料的掌握與基本的分析應用，彷彿已成為電腦成長世代中必須具備的基本技能。君不見坊間各類有關大數據、資料科學分析的文章報導、書目、工作坊、課程、研討會等等正夯。連本人也不能不免俗地栽半個頭進去探探data analysis是什麼東西。  
  
舊曆年前，科技報橘上刊了一篇：[人人都可成為資料科學大師！一整年的網路自學清單](http://buzzorange.com/techorange/2016/02/02/plan-to-be-a-data-scientist-in-new-year/)，不失為某種平靜中肯的技術學習建議。但是對於我這個教育改革前，數學程度只停留在高中社會組（且絕大多數已忘記），其實在自學程式語言與資料科學的過程中，現在反而是花更多時間在回顧、學習大學時代必修的微積分與統計學等觀念，然後就卡關卡很久。  
  
昨天看到一個綱站：https://www.databasic.io/en/ 站如其名，宣稱要從資料數據的基礎ABC入門，讓初學者一步步了解使用資料利用資料的神奇妙處與核心概念。我照著走過一遍綱站上示範的三種線上工具使用來呈現數據分析的結果，讓我連結到過去一年來閱讀過某些文章案例，似乎讓我多少更明白了資料數據可以怎麼使用的各種變化，故在此野人獻曝地稍作點筆記分享：  
  
[www.databasic.io](https://www.databasic.io/en/)目前展示了三個線上工具，讓使用者借著互動式的操作，體會一下資料數據的妙用。換句話說，這個網站的目的不是在教讀者如何寫程式工具以作資料分析，程式工具網站已經作用了，這裏就只是單純地讓使用者進行實際操作。  
  
1. word counter  
以第一個示範工具數字計算與頻率出現次數視覺化。這馬上令我直接聯想到，台灣2016選舉年前，傳統藍綠兩大黨之外的所謂第三勢力並起，Torrnet利用統計軟體 R語言作初步檢測，寫了一篇： [第三勢力很難挑嗎？臉書大數據分析呈現的政治與政策傾向](http://blog.roodo.com/torrent/archives/46998642.html)。該文章前半段使用的關鍵字頻率（term frequency），不正這個word counter 的標準範本嗎。   
  
2. WTF csv  
至於第二個工具，利用收集來的csv檔案（cvs為纯文本形式儲存的表格數據資料）到底有什麼眉角。去年英國開放大學在Future Learn上開設了一門： [Learn to Code for Data Analysis](https://www.futurelearn.com/courses/learn-to-code)，介紹如何利用程式語言python以及其強大現成的函式庫工具（library），來作各種資料的分析與結果視覺呈現。四週的課程進度並不要求學習者事先具備任何程式寫作能力，故其介紹python使用上，會略過許多基礎的功能介紹，而強調在如何引進函式庫工具，讓別人寫好的程式碼輕鬆替你達成各種要想的功能目的。  
我以當時課程中使用的案例csv檔案（2014年英國城市倫敦一整年的氣候記錄資料）作範本，看看利用WTF cvs工具成跑出什麼東西，  
結果在365天（row）對應的23個（column）氣候觀測項目,就跑出了[23個統計圖表](http://www.databasic.io/en/wtfcsv/results/56be9dc4a0d97b004533c7bc?submit=true)。  
[![csv-london2014](https://4.bp.blogspot.com/-__x2TzJUD9c/V30itSp29tI/AAAAAAAAKQc/oMwAnyXQz2IQr7HVml_lAO1XA550WgoiACLcB/s320/Screenshot%2Bfrom%2B2016-07-06%2B23%253A24%253A13.png)](http://www.databasic.io/en/wtfcsv/results/56be9dc4a0d97b004533c7bc?submit=true)  
  
3. Same diff  
第三個工具呢則是讓使用者可以上傳二個文字類型的檔案來作文本相似度的比較分析,並且可下載這二個文字檔各自出現單字的次數統計表單（csv）。這讓我想到了Google 與英美幾所大學法學院合作推動的世界各國憲法文本比較資料庫計畫：[Comparative Constitutions Project ](http://comparativeconstitutionsproject.org/)，除了研究者初步做成的憲法文本資料外，去年底還公布了一個線上的各國憲法資料庫與線上文本比較工具網站： [https://www.constituteproject.org/](https://www.constituteproject.org/)  
  
  
另一個更「誇張」的文本資料內容探勘分析計畫，則是有美國學者提出針對國會或各州立法議會的草案或決議文版本進行電腦比對分析，來追究其背後可能利益團體與政治角力。[When Lobbyists Write Legislation, This Data Mining Tool Traces The Paper Trail](http://www.fastcoexist.com/3051823/when-lobbyists-write-legislation-this-data-mining-tool-traces-the-paper-trail)  
  
當然same diff 的功能還是比較陽春，無法做到後二者計畫如文字出現次序，前後連貫性等比較，不過從這個簡版型的資料分析出發，但倒是對新手有不少啟發吧。我試了一下，可惜目前Same diff未支援中文字碼的文字檔。

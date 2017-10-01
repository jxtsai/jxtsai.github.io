---
author: jx tsai
comments: true
date: 2016-07-28 02:56:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/07/28/datadesign%e6%95%b8%e6%93%9a%e8%b3%87%e6%96%99%e8%a6%96%e8%a6%ba%e5%8c%96%e5%85%a5%e9%96%80%e6%9b%b8/
slug: datadesign%e6%95%b8%e6%93%9a%e8%b3%87%e6%96%99%e8%a6%96%e8%a6%ba%e5%8c%96%e5%85%a5%e9%96%80%e6%9b%b8
title: Data+Design數據資料視覺化入門書
wordpress_id: 43
categories:
- advocacy
- DataAnalysis
- tactical technology collective
---

因為上了Advocacy Assembly有關倡議[訊息視覺化](http://self.jxtsai.info/2016/07/advocacyassemblyorg.html)的入門介紹，想再看看其推薦的材料「Data Visualization」手冊內容,稍仔細閱讀其內容之後才發現這本書其實在一年多前就知道它的原始碼被釋出在[github](https://github.com/infoactive/data-design)上面，自己還fork這個專案一度想來進行中文在地化的工作（幸好當下只想了十秒鐘，然後立即放棄此念頭XD）。這兩週來因為自己一邊讀Schoo of Data的課程一邊整理筆記，順手查了一下華文世界有關數據資料應用的狀況，才知道g0v臨時政府有人號召展開本書的[正體中文化翻譯工作](https://www.gitbook.com/book/g0v/data-design/details)（工作平台是github底下，再透過gitbook展現成果）。另外，對岸的「字幕組」XD已完成了[簡體中文化的全文翻譯與排版上線](http://dataunion.org/book/datadesign/)，較習慣中文閱讀者可以先睹為快。  
  
![](https://4.bp.blogspot.com/-YtqakXe4OPg/V4zSKcfOB5I/AAAAAAAAKfQ/QJE2cQWEh5wJBcvfJbXnbJJFO8FyqSD0gCLcB/s1600/designdata.png)  
  
如今終於不認真地把下載多時的檔案讀完，故本文稍來介紹一下我畫的重點和感想。  
雖然本書標題欲平衡「設計＋數據資料」二者的重要，本書多位協力作者中其實背景還是比較偏向於「設計」為重，這點在書名上的排序雖以「資料」為先但內容比重還是多強調「設計」。再者[網頁呈現上](https://infoactive.co/data-design/titlepage01.html)就可以看出其風格，完全是近兩年網頁強調回應式（responsive）、簡潔、大區塊的風格。另外網頁上也提供了多種檔案格式的電子書（如pdf、mobi、epub　），我自己先讀了PDF電子書，但發現其中某些案例提供的數據資料在PDF的文本分析中有些怪異，回頭查網頁版的資料才知道ＰＤＦ中並未完整呈現某些表格，猜想可能是直接利用轉檔工具時出了問題，故建議還是直接在網頁版上閱讀好了。  
  
本書分成五大部份分別為：一數據基礎Ｄata Fundamentals、二收集數據資料Collecting Data、三準備資料Preparing Data、四數據視覺化visualizing Data、五提醒What not to do。其實前面３部份的內容和School of DATA的「數據入門」、「數據清理」、「數據探查」這三門課程內容大同小異（請另見本人整理的介紹： [![](https://3.bp.blogspot.com/-K6E6VwLwpyk/V5lyl-naWZI/AAAAAAAAKmc/w_OqZzxszBYUeM3LGW37AfPJrUEuht1agCKgB/s320/Damned%2BLies%2Band%2BStatistics.jpg)](http://www.ucpress.edu/book.php?isbn=9780520274709)[School of Data -1 數據資料入門20160714](http://self.jxtsai.info/2016/07/school-of-data-1.html);[School of Data -2 數據清理入門20160717](http://self.jxtsai.info/2016/07/schoo-of-data-2.html), [School of Data -3 數據探索之道20160721](http://self.jxtsai.info/2016/07/school-of-data-3.html)），只是後者比較偏示範面案例操作How，而本書則比較多文字解釋來說明：為何Why、為什麼What、 對象是誰Who等問題思考，就看讀者自己的興趣與好奇何在吧。其中第二部份「收集數據」（Collecting Data），是ＳＯＤ的數據三大入門課裏較少提及的，本書主要介紹不同類型的數據資料其最佳最適的收集方式，收集來源當然也有所差異。這部份前面二大單元處理的是問卷調查（透過本身第一手的資料收集工作），故提介了問卷調查基本目的、如何設計問卷並找到目標對像進行調查與回應收集。而第三四部份則是放在非初級一手資料的取得，尤其提醒研究者／報導者在使用這類資料之前須做好必要的檢查確認，並標明資料引用來源與作者。這一點似乎在華文世界中比較不被重視，倒是可以好好參考下本書在這個地方的重要提醒。第五單元是如何把數據資料視覺化，最後一個單元（六）則是提醒在將數據視覺化時千萬要留意一些容易犯的錯誤,不要也跟著失足。（最近讀完「[Damned Lies and Statistics: Untangling Numbers from the Media, Politicians, and Activists](http://www.ucpress.edu/book.php?isbn=9780520274709)」，作者Joel Best以「糟糕的統計」（bad statistics）案例出發，揭示許多隱藏數字與統計陷井背後的問題,讓讀者打破數字盲innumeracy,不要被政府或社會運動者提出的數字給唬住了，很精采有趣，大推！！ ）  
  
本書大約用了一半篇幅來介紹數據視覺化之前的前置作業：認識數據、如何收集數據、清理整理數據等基礎準備工夫。好了，接下來總算可以進入第五單元「正宮話題」：數據資料視覺化（即設計design）。本文稍多著墨一下該單元對於資料視覺化的處理程序的整理，又細分為ＡＢＣＤＥ如後。不過老實說我讀過後，反而建議不如直接去上[Advocacy Assembly](http://self.jxtsai.info/2016/07/advocacyassemblyorg.html)二門有關倡議視覺的入門課程（各90分鐘）：「Design for change: Graphic design for human rights」、「Data for change: data visualisation for human rights」，這兩堂其實更具體地書中提及在處理視覺化時的注意要點簡明以多媒體方式介紹帶出了。  
  
A) Deciding Which and How Much Data to Illustrate 決定哪些資料需要呈現  
在數據視覺化的過程中，首先要決定哪些資料、多少的數據要放入視覺化方案中。因此第一步就要先想清楚要如何呈現資料，也就是要先弄明白兩大問題的答案：到底要傳播出什麼樣的訊息內容，以及設定的觀眾對像是誰？這時候不妨重新跳出雜亂的數據與成堆的資料中，問問自己：我知道了什麼？它代表著什麼意義？為何這件事是重要的？盡量深掘，更具體鎖定問題，好讓你找到的答案更為精確精準。當找一個合理、精準、可說服人的答案，又如何把這個答案轉換成一個具吸引力的一條訊息？當思考訊息內容時，具體想像要訴說對話的設定讀者對象就很重要了,因為讀者對象的不同，訊息的難易、面向、調性也自然會跟著調整。清楚了目標觀眾的屬性與可能偏好後，不妨自問：對這些人而言，什麼是最有價值的訊息資訊？因為對其有價值才會對他們創造吸引力。  
  
B) Graphing the Results of Checkbox Responses    
其實我不太懂這章的重點在講什麼＠＠，字面上是提醒讀者在問卷調查設計時如果使用多選項式的答案勾選，其在作後面的滙整統計上可能會出現比例加起來超過100％的狀況，要如何地再重整資料之類的。  
  
C) Anatomy of a Graphic 圖表解析  
這章雖然名之為「圖表解析」，但沒怎麼提及在決定如何把數據資料轉換成為圖表樣式之間，有什麼可參考的原則（這點反而是SOD與TCT作的教材整理的比較清楚），倒是著重在圖型座標資訊（意義、單位）。  
  
D) Importance of Color, Font, and Icons 顏色、字型與圖示的重要性  
這裏在探討某些設計原則、合適工具以進行視覺化過程的補強或修正，以加深閱讀視眾的感官體驗及對數據資訊與欲傳達訊息的理解，其大致可以分透過字體字形的辨識性與可讀性、版面安排的層次、構色等三方面來介紹。  
a) 字體字形　Fonts & Text：  
b) 版面安排層次 Hierarchy：其涉及到我們如何權衡與組織條理資訊，有清晰的層次感設計可讓讀者清楚地了解如何來有先後次序地來處置解讀資訊。  
c) 構色Color:顏色的運用可以放到最後再做考慮，因為一份成功的視覺化作品是建立在線條、形狀、明暗、版型與結構等構成圖像等元素之間的平衡。而顏色則是在完成這些事實建立的和諧後，再賦予圖像更完整的豐富性。  
  
Ｅ) Print Vs. Web, Static Vs. Interactive 視覺化成品的呈現形式：印刷紙本或網頁版？靜態或互動式？  
  
讀完本書後，總覺得有許多地方僅是點到為止，令我有一種不痛不快之感？也讓我想起一年多前差不多同一段時間前後，先讀完的另一本相似談視覺倡議的指引書「[Visualising Advocacy](http://self.jxtsai.info/2014/11/visualising-information-for-advocacy.html)」,當時讀完後雖然寫了一篇簡單的介紹（從標題來看，似乎曾經企圖寫多篇介紹，但至今難産中？）一如自己的文章也是同樣是不痛不養之感，故趕快再重新下載該書來回憶一下它的結構與內容。Visualising Advocacy的重點比較放在「視覺化」的討論上，故很適合和「Data+Design」討論設計的部份一起搭配閱讀。VD雖然也有一小部份討論了資料數據，但並沒有進入太過瑣碎的數據收集、數據整理等ABC的細節，反倒是對於在魔鬼藏在細節裏作了不少的提醒與建議。因為Visualising Advocacy並未整理目錄頁，故先簡單地整理一下它的目錄與章節架構，讓讀者稍有一點概念其編寫時的想像大約是這樣：  
  
A)Introduction 前言介紹  
B)Elements of Visual Persuasion:Information, design, networks & technology 視覺說服的組成要素  
C)Forms of Influence:Interruption, education & coercion 倡議行動的介入方式  
D)Get the Idea: 開著準備進行視覺化處理  
E)Get the Picture: 針對資料與視覺提案進行各種測試實驗  
F)Get the Detail:這部份雖然是討論數據資料的處理細節，但不會像介紹數據資料入門使用太多統計或試算表工具，而是偏重對於某些容易忽視處的提醒。  
G)Putting it into Practice：再次進行策略分析，好理清運動理念、訴求對象、手段、溝通方式等思考和應用  
H)Resources：相關視覺化工具的整理清單   
  
![](https://3.bp.blogspot.com/-O71AINRTpR4/V5lzlEhyJJI/AAAAAAAAKmY/mmnU4Ub5UzsQ7E7HZxmgDDJaenSjDrAkQCLcB/s1600/Visualising%2BAdvocacy.jpg)   
  
我會在另一篇文章中好好整理Visualising Advocacy這八大單元的內容（握拳），至少其中B～E的部份探討了許多在進行視覺化設計時可以參考的技巧與策略，值得另外再作仔細介紹。

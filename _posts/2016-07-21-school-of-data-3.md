---
author: jx tsai
comments: true
date: 2016-07-21 04:42:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/07/21/school-of-data-3-%e6%95%b8%e6%93%9a%e6%8e%a2%e7%b4%a2%e4%b9%8b%e9%81%93/
slug: school-of-data-3-%e6%95%b8%e6%93%9a%e6%8e%a2%e7%b4%a2%e4%b9%8b%e9%81%93
title: School of Data -3 數據探索之道
wordpress_id: 47
categories:
- DataAnalysis
- schoolofdata
- tactical technology collective
---

School of Data 第三門課程名為：A gentle introduction to exploring（數據探索之道）。前二門課程「[數據資料基礎](http://self.jxtsai.info/2016/07/school-of-data-1.html)」和「[數據清理](http://self.jxtsai.info/2016/07/schoo-of-data-2.html)」是讓初學者了解如何利用試算表工具來整理表格、清理數據，運用軟體內鍵函數等技巧技術，也應該在清掃數據的過程中，體會到資料類型的重要區別，盡量遵守共識規則來處理數據記錄的重要性。而接下來的這門課程則將會進一步帶領學習者來體驗認識試算表工具底下pivot table 的基礎操作控制知識，透過約20道習作題目的自行練習操作，來熟悉了解pivot table的妙用，好讓初學者經此工具的輔助，更輕鬆地進行數據探索的旅程。除了花時間在試算表pivot　table的介紹體驗外，這門課另一半則是處理ＳＱＬ的學習，讓初學者練習從圖型介面操作的舒適區開始慢慢滑入文字指令的深水區囉～～  
  
以下就針對本門課程所畫分的四大單元再作點概要整理：  
  
1)　A gentle introduction to exploring and understanding your data  
介紹試算表的資料透視表（pivot table）。以前從不知道Excel等試算表工具底下還有這pivot table功能，google spreadsheet把它的中文譯為「資料透視表」，而在EXCEL底下好像叫做「樞紐分析表」（據說還有暱稱其為「飄忽分析表」）。簡單來說，它的功能就是在一大張（欄列很多，各種分類、項目、戳記等等）試算表中，可讓使用者進一步決定要挑選哪幾個認定要先檢查分析的資料欄列，把它特別挑出來查看這些指定資料之間的關聯性，試算表還是自動給這些資料作分類。我個人在試作的過程中覺得最有趣的，就是可在 pivot table 底下把原始表格的欄列移來移去，每一次改變資料的呈現，其背後似乎都有著更深的故事可以去探掘。絕大部份介紹試算表或數據分析的課程，多是以股票漲跌、公司收支利潤為示範案例。但本課程中預設學習對象可能是NGO工作人員或社會議題關心者，故以NGO組織GRAIN的所作的2012年全球土地掠奪狀況數據為分析示範樣本。如果對土地正義有感者練習這份資料數據，心中一定會激發出許多想法。譬如說是哪些跨國企業在哪裏佔用土地資源、其土地利用目的用途、投注經費、計畫階段等資料。  
![](https://1.bp.blogspot.com/-MS5bAmYlGA4/V5ApXFkrRdI/AAAAAAAAKgA/3zS6J6_VrJYluMJa1Lh-KqnTaBi6l4rHwCLcB/s1600/pivot45.png)  
  
2) Advanced Spreadsheet Formulas 試算表的進階公式計算與內建函數應用  
SPLIT, SUBSTITUTE（其功能作用已在上篇作了整理，但在LibreOffice Calc似乎沒有split函數,若要進行同一欄中多筆資料的分割，多是叫出data/text to columns這個功能來進行）  
  
=VLOOKUP(SearchCriterion; Array; Index; SortOrder)：參照右方相鄰的儲存格之垂直搜尋。此函數的第一個參數為：數據比對的依據值，通常為某儲存格，作為檢查第二個參數即陣列，其寫法為Sheet2!C:D(Sheet2為要查找的試表算Sheet2的查找範圍限於C,D二欄，若在同一個試算表則為C:D)的第一欄是否包含特定值。接著，此函數會傳回 Index 指定欄之同一列中的值。若忽略 SortOrder 參數，或將參數設定為 TRUE 或 1，則假定資料依向上排序。此時，如果找不到完全相符的SearchCriterion，則會傳回比條件小的最後一個值。若將 SortOrder 設定為 FALSE 或零，則必須找到完全相符的項目，否則結果會是錯誤 Error: Value Not Available (錯誤：數值不存在)。因此，資料值若為零，則不需要依向上排序。  
  
3) An Introduction to SQL Database for analysing data - part 1  
雖然前面介紹了試算表的內建函數、表格資料透視分析等功能，讓習慣圖型介面操作的使用者可以好好地分折研究數據資料，但是試算表卻有其不足，尤其在處理大型巨量數據上更為吃力有限，如果以類比來作說明，試算表只能處理單一試算表格，但資料庫卻可以處理運作多重表格的資料結構，故接下來的二章則以介紹資料庫最流行的結構查詢語法（ＳＱＬ）  
這個單元先是介紹進入SQL之前的準備工作：如何在電腦上安裝免不用附在伺服器套件下的SQL輕量版SQLITE。因為我已改用ubuntu作業系統，linux真的比蠻windows更適合進行文字指令環境。只要叫出端終機程式，看看是否有安裝了SQLITE($sqlite3)，如果沒有，它也會提示利用apt-get install sqlite3進行安裝。  
  
安裝好SQLITE3之後，這節就是簡單地練習如何在SQL底下新建一個表格table, 表格欄位的資料類型與值設定、如果把資料放入表格中等等基本語法。我比較看不懂的是如何把作成的資料滙出，查了一下指令要這樣下：  
sqlite> .mode csv (csv為要滙出的檔案格式)  
sqlite> .output people.csv (people.csv為要滙出的檔案)  
sqlite> select * from people; （把表格people上的資料全部抓出來）  
然後就可以看到目前所在的工作檔案目錄下多了一個people.csv檔案，其內容完全和利用SQL語法建立的表格一致  
![](https://4.bp.blogspot.com/-2YaI7jJR98M/V5AwLUB2WDI/AAAAAAAAKgQ/K5q48DMVs0Q-IEKhvUsPgFtaZPHeoIv0QCLcB/s1600/Screenshot%2Bfrom%2B2016-07-21%2B10%253A14%253A48.png)  
  
4) An Introduction to SQL Database for analysing data - part 2  
了解文字指令介面下的SQL基本語法操作後，接下來就是要進一步介紹如何利用SQLite做數據的分析。這裏它用了一個１百多ＭＢ內含100多萬筆在挪威註冊登記的公司資料為操作示範。嗯，不知道別人電腦的效能如何，但在我2009～2011年出廠的中古舊型筆電上，用LIBREOFFCE CALC來開這個檔案肯定是要當機的，由此可知SQL處理大型數據資料的強處優勢何在。不過因為是文字指令操作環境，可能要花一點时間想像和習慣到底要在這個數據庫裏面找什麼東西，如何來分析。   
  
我個人感覺本單元後來部份處理的比較零亂，尤其在中後段它的SQL程式碼已經不再只是一二行而是突然增加三四倍，來到了十來行的長度，初學者可能會看得頭昏腦脹。建訪不妨同時也多到其所推薦的閱讀清單，到 [SQL動物園](http://sqlzoo.net/wiki/SQL_Tutorial)來多作點練習。  
  
如果還是習慣圖型介面者，有一個瀏覧器的外掛（[sqlite manager](http://lazierthanthou.github.io/sqlite-manager/)， 供應firefox, chrome版本），也不需要安裝伺服器而可以用來解析sql檔案。雖然它是在瀏覧器下分頁的圖形介面環境，但還是得會一點基本的ＳＱＬ語法才知道如何下指令操作資料庫。  
![](https://3.bp.blogspot.com/-CPBU4gi0E7U/V5AxfXf8gdI/AAAAAAAAKgc/vyMLxPIl1iUsHmvBTKa6t8hwzJ1mLvBHACLcB/s1600/SQlite%2Bmanager.png)  
  


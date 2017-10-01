---
author: jx tsai
comments: true
date: 2016-08-08 23:50:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/08/08/school-of-data-4-%e5%be%9e%e7%b6%b2%e8%b7%af%e4%b8%8a%e6%8a%93%e5%8f%96%e6%95%b8%e6%93%9a/
slug: school-of-data-4-%e5%be%9e%e7%b6%b2%e8%b7%af%e4%b8%8a%e6%8a%93%e5%8f%96%e6%95%b8%e6%93%9a
title: School of Data -4 從網路上抓取數據
wordpress_id: 33
categories:
- DataAnalysis
---

School of Data的數據資料入門系列已經介紹過了：基礎入門（[School of Data-1 數據資料入門20160714](http://self.jxtsai.info/2016/07/school-of-data-1.html) ）、清洗整理數據（[School of Data -2 數據清理入門20160717](http://self.jxtsai.info/2016/07/schoo-of-data-2.html) ）、使用試算表pivotal table功能進行分折以及SQL資料庫結構式關係語法學習等（[School of Data -3 數據探索之道](http://self.jxtsai.info/2016/07/school-of-data-3.html) ），可說掌握了基礎數據資料處理概要。而接下的ＳＯＤ課程的課程則會偏向利用主題式數據資料（如新聞學與數據、財政資料剖析、國際援助數攄）與技術提醒（如地理資料，網頁爬蟲抓取資料等）。  
  
School of Data在一開始的[數據基礎課程](http://self.jxtsai.info/2016/07/school-of-data-1.html)中，就提過資料從何而來？----自身第一手的資料收集調查到二手的開放公共資料（特別是公部門），另外也有民間倡議的開放資料分享集散資源中心等等。二手資料的取得來源，除了後兩者本身就是以提供開放資料的進用再利用為目的，所以可以先假設其提供的數據資料多為清理過、機器可讀的檔案型態（姑先不論資料本身的「真實」與「正確」與否）。然而除了這類稍具系統與規模化的公開資料外，大部份的研究或調查，還是得另闢蹊徑,由作者或提問者另從各種管道與方式來訪查收集一二手資料。其中網路就是一個很好的媒介，可能找到許多相關的數據資料。但這些個別成章各家之言，甚致有點雜亂散佈的資料，如何把它㧓回自己的電腦上，讓它可以用來被用於解讀分析之前，要透過什麼工具和技巧來粹取數據呢？這即是SOD系列課程四的網路數據抓取介紹，其基本上有二大部份，一是對於PDF檔案格式的轉換，一是如何處理網站網頁型資料的抓取。  
  
1. Extracting data from PDFs using Tabula 利用Tabula免費開源軟體來萃取PDF檔案格式。  
PDF其英文全名為Portable Document Format，一種用獨立於應用程式、硬體、作業系統呈現文檔，也是網路上最常見的文本檔案格式。故許多從互聯網下載的資料多儲存成此格式，其雖便於閱讀，但並不易直接讓機器電腦識讀運算。故Tabula便因蘊而生，這個運行在JAVA底下的跨平台PDF檔案粹取工具，能抓取PDF檔案中的資料（文本、表格等），並將之轉換為機器可識讀的檔案格式如CSV, JSON, TSV, Scripts, zip(CSV壓縮)等。這個軟體操作介面直覺好用，不過也有其限制，像是Tabular無法㧓取圖片掃的ＰＤＦ格式檔，只能支援由電腦轉成的PDF,另外如果原本在表格製作時，儲存格有合併或是多列，則可能在滙出時也會出錯。  
  
似乎在處理中文內容時，也特別容易發生問題。(還是怪公務員使用excel時為了把檔案弄得看起來美美的，總是亂合併儲存格啊？)  
![](https://3.bp.blogspot.com/-XVaQaU3_TzM/V47c-g_RqXI/AAAAAAAAKfg/7HMSuRMFI90AsfQarBIB40qR604T7dfDQCLcB/s1600/tabula.png)  
  
其它參考中文資料：　[不知道怎樣把 PDF 表格轉資料嗎？ 讓 Tabula 解救你！](http://blog.infographics.tw/2015/06/extract-table-from-pdf-by-tabula/)（出處：資料視覺化）  
  
2. Making data on the web useful: scraping 抓取互聯網中ＨＴＭＬ格式的表格資料  
SOD提及了二個方法來抓取網路上的表格資料，一個是利用Google spreadsheet內建importHTML，一個是利用Chrome 瀏覧器上的外掛套件工具scraper。  
  
A) importHTML  
html 上的表格資料，可利用Google spreadsheet功能：importHTML來進行HTML檔案格式中的表格資料抓取，並把資料滙入到Google spreadsheet試算表上以利進一步利用。  
  
其函數公式為：=importHTML("","table",N)  
第一個參數為資料網址,即在兩個上引號之間填入抓取的表格之網址資訊  
第二個參數則為要㧓取的網頁要素（element），這裏當然填的是"table"  
第三個參數則為要㧓取的網頁上，html要素表格中的第n個表格。  
  
https://support.google.com/docs/answer/3093339?hl=zh-Hant  
  
這個方法雖然好用，但是如果目標是中文網頁資料，則google spreadsheet引入的表格常會發生亂碼。有網友[寫出轉換編碼預設函數，來解決中文編碼問題](http://shanhua0131.blogspot.tw/2015/03/importhtml.html)。我自己也試著照做了一番，但卻一直沒法成功呈現BIG5編碼┴─┴︵╰（‵□′╰ (主因是我不知道如何把spreadsheet底下自編的腳本函數順利地編譯發佈來被使用)  
  
B) Chrome Extension: scraper  
利用Chrome 瀏覧器上的外掛套件工具scraper https://data-miner.io/(目前只有chrome版本，未有firefox恨～～)  
這個工具雖然很直覺好用，但使用者得先註冊登記（以google帳號），才能取得完整的數據抓取結果。初步試驗，這個外掛在呈現中文時一切正常，倒是如果網路資料本身撰寫時沒依照規範格式，也無法完整顯示資料。以我試著抓立法院的會議預報公告，雖然網頁看起是表格式（時間、主席、議程、地點），但利用scraper抓取時卻只能出現單欄資料內容，我猜這可能和立法院的網頁編寫樹枝狀架構有點混亂，讓程式在判讀時無法把其它欄位視作同一階層的子節點而抓下來。（反正要怪罪別人就是了）  
![](https://1.bp.blogspot.com/-SX6J2QIDSso/V47pVGLRqJI/AAAAAAAAKfw/LpMCgvkSq7oHG-enQIOKMqdBuVScc-1bACLcB/s1600/scrapper.png)  
  
3. [Beyond the Basics 從互聯網抓取資料進階焋篇](http://schoolofdata.org/handbook/recipes/scraping-beyond-the-basics/)  
前面是套用現成的工具軟體或已寫好的函數來抓取資料。而在SOD手冊資源的進階篇「Beyond the Basics」則需要有點基本的網頁文本資料格式知識（如xml、json）與程式編寫能力(javascript, python)。  
例如slate, pdftohtml, xpdf為python寫成的函數庫,從名稱上可以猜出它們的功能就是把PDF文件內容粹取成為純文字檔或是html格式。（試著安裝使用，但似乎因我的python缺少另一個相關函數庫而無法使用slate函數功能）  
  
我個人覺得School of Data在前三個入門系列之後，接下來的線上課程內容其實慢慢變得有點雜亂無章。不過我還是會盡量整理我的學習筆記吧。  
  
  
  


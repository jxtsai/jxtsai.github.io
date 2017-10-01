---
author: jx tsai
comments: true
date: 2016-06-05 15:36:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/06/05/recuva-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97/
slug: recuva-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97
title: RECUVA 工具指南
wordpress_id: 69
categories:
- localization
- opensources
- Security First
- umbrella app
---

[Security First's umbrella app](https://secfirst.org/) 中電腦工具指南的倒數第三篇（其實還有四篇，但都是介紹ＰＧＰ電子郵件加密，只是因有Windows, Linux, Apple OSX, Adnroid 不同作業系統而分別說明介紹）。這個工具我個人未使用過，無法作什補充，倒是它應該有支援正體中文的語言包版本，網路上其它中文的介紹教學文也不難找。  
  
***本文為Security First製作的手機應用umbrella app正體中文化翻譯系列資料之一。目前仍為初稿狀態，虛心接受指正批評。原始的json資料格式配合app電子書的html編輯標籤，轉貼到部落格上排版混亂也欠缺原始圖檔請見諒。***  
**Recuva Tool工具指南:資料恢復與安全刪除**  
  
![recuva](https://4.bp.blogspot.com/-478C_jTOrj4/V34m89GHHCI/AAAAAAAAKTw/ks2RzGRjxBslW0dhdmSDUDxBMYSNRJy7ACLcB/s320/recuva-1.jpeg)  
**學習內容: [「備份」](umbrella://lesson/backing-up)**  
**軟體下載處:** [http://www.piriform.com/recuva/builds](http://www.piriform.com/recuva/builds)    
**電腦系統要求:** 任何版本的Windows作業系統   
**本指南中使用的軟體版本:** Recuva 1.3  
**版權宣告:** 自由軟體  
**程度:**中級  
**所需時間:** 20 分鐘  
**Recuva 可以:**執行不同的掃描模式；試圖回復電腦上稍早被刪除的檔案,包括電子郵件、圖片以及影片等；安全地刪除私密敏感的資料。Mac OS使用者可以選擇[TestDisk and PhotoRec](http://self.jxtsai.info/www.cgsecurity.org/),作為替代的類似備份工具,其也有相容於Microsoft Windows and GNU Linux的版本.  
**1.1 開始之前**  
當遇上了敏感或私密資料意外被刪的情況, Recuva可以協助掃描與部份重建.如同在**[「刪除」課程](umbrella://lesson/safely-deleting)**裏的介紹, 在標準的Windows 作業系統的刪除功能刪掉一個檔案, 即便資源回收筒已經清空,但檔案仍然存在電腦上.但是有些狀況下Recuva還是無法回復這些資料. 如果是執行CCleaner 安全的檔案刪除選項，這些檔案就真的回不來了. Recuva無法回復像CCleaner 或 Eraser等軟體所清理的檔案以及由Windows本身已經覆寫了原本檔案所佔用的空間. Recuva 也無法回復損壞的文件和檔案.Recuva 可用於安全地覆寫私密或敏感的資料磁區.  
  
**2.0 如何安裝RRecuva**  
**第1步.**雙擊檔案“rcsetup138.exe”;可能會出現 _「開啟檔案」Open File -「安全警告」 Security Warning_的對話視窗. 這種情況下點擊「執行」“Run”以激活語言方框.  
**第 2步.** 點擊“OK”以進入 _Recuva 「簡易設定」“Setup Wizard”_歡迎畫面.  
**第3步.**點擊「下一步」 “Next”進入_版權協議_畫面. 請閱讀_版權協議_內容後再進行接下來的安裝程序.  
**第 4步.** 㸃擊「同意」“I Agree”，進入_「選擇安裝」“Choose Install”_位置的畫面.**第5步.**點擊「下一步」“Next”，進入_「安裝選項」“Install Options”_.  
**注意:** _「安裝選項」“Install Options”_畫面也會出現是否_「安裝Yahoo工具列」“Install optional Yahoo! toolbar”_選項. 請_不要_安裝 Yahoo!工具列 toolbar, 它可能會損害你的網路隱害與安全.  
**第6步.**檢查_「安裝Yahoo工具列」“Install optional Yahoo! toolbar”_的選項是否取消，其畫面如下:

![](http://self.jxtsai.info/tool_recuva1.png)  
**第7步.**點擊 「安裝」“Install”開始安裝Recuva.當安裝程序完成後，其安裝進度條會自動消失.**第8步.**點擊「完成」“Finish”以結束安裝Recuva.現在已成功地在電腦上安裝好了Recuva,可以安心地開始來覆寫與恢復私密或敏感的資訊  
  
**如何利用HRecuva執行各種掃描  
3.0 開始之前**  
這部份, 你會學到如何執行不同類型的掃描方法,並了解在_「選項」“Options”_底下 _「一般」“General”_與_「行動」“Actions”_分頁的功能. **注意:**掃描是簡單地回收顯示出潛在可能回復的檔案.真正的回復過程將在下一部份作介紹.  
**  
3.1 如何利用Recuva 精靈執行掃描**  
當不知道想要回復的檔案全名或是只記得部份檔名時，建議使用Recuva _「精靈」“Wizard”_ 來掃描. 若是初次使用Recuva，也建議利用其精靈功能. Recuva _「精靈」“Wizard”_ 可設定掃描參數，如指定檔案類型或檔案被刪除的原位置.開始掃描被刪除的檔案,請執行以下步驟:  
**第1步.**點擊Recuva圖示或從「開始」“Start” >「程式集」“Programs” > Recuva > Recuva來啟動該軟體,啟動後會出現以下的畫面:

![](http://self.jxtsai.info/tool_recuva2.png)

**竅門:**如果你知道要回復檔案的完整檔名或部份檔名,請點擊「取消」“Cancel”而到使用者主選單下的_“Piriform Recuva”_,然後再依照第3.2部份的「如何不透過Recuva精靈來執行描掃」介紹.  
**第2步.**點擊「下一步」“Next”將出現以下畫面:![](http://self.jxtsai.info/tool_recuva3.png)_Recuva Wizard File type_會顯示出一份不同類型的檔案清單, 以及描述當每一種功能啟動時，什麼樣的檔案可能會回復.  
**第3步.**檢查_「其它」“Other”_選項, 然後點擊「下一步」“Next”，即會看到下面的畫面：![](http://self.jxtsai.info/tool_recuva4.png)**注意:**_「Recuva精靈檔案位置」“Recuva Wizard File Location“_的預設設定是_「不確定」“I'm not sure option”_選項.這個選項會讓掃描延伸到所有硬碟磁區包括可移除的行動裝置,但不包含CDs, DVDs 光碟機與光纖式媒體.因此它將會花上較長的時間來取得結果.Windows 作業系統下沒有經常自資源回收筒刪除檔案的話, 可大量減少意外誤刪私密或重要資料的機會.  
**第4步.**檢查_「資源回收筒」”In the Recycle Bin“_選項後,按「下一步」”Next“會看到以下的畫面 :![](http://self.jxtsai.info/tool_recuva5.png)**注意:** For this exercise在這個練習中,不要啟動了_「深度掃描」”Deep Scan“_選項.我們會在3.3 部份「如何執行深度掃描」中提到.  
**第5步.**點擊「開始」”Start“以進行回復刪除檔案程序.在檔案回復過程中,在快速演替中會出現兩個進度狀況條.第一個是:_「掃描磁區」"Scanning the drive for deleted files“_ 進度條會列出被刪除的檔案清單. 第二個:_「分析檔案內容」“Analyzing the file contents”_進度條則會分類與整理出被刪檔案之類型以及可復原程度.  它們也會顯示掃描與分析的時間與過程. 使用者主選單下的_“Piriform Recuva”_介面可能變成以下的樣子:![](http://self.jxtsai.info/tool_revua6.png)使用者主選單介面_Piriform Recuva_會出現一個六欄表格，列出每一筆被刪除檔案的資訊.每一個欄位的介紹如下:

**「檔案名稱」“Filename”**這裏會顯示出被刪除檔案的完整名稱以及其副檔名.點擊_「檔案名稱」“Filename”_的標題會重新把檔名以字母次序排列.**「路徑」“Path”:** 這會顯示出被刪除的檔案是在哪裏找到的.在這個例子中，因為啟動了_「資源回收筒」“In the Recycle Bin”_選項, 所以被刪除檔案的路徑是_C:RECYCLER_.點擊 C_「路徑」“Path”_的標題可以檢視列在某一個特定目錄或檔案路徑上的所有檔案.**「上次修改」“Last modified”:** 其顯示檔案被刪之前最後一次修改的時間,它可以幫助你辨別出想要回復的檔案.點擊_「上次修改」“Last modified”_ 可依最久或最近的時間列出被刪除的檔案清單.**「檔案大小」“Size”:**它會顯示檔案的大小.點擊_「檔案大小」“Size”_會依照被刪檔案的大小而整理出被刪檔案清單.**「狀態」“Status”:**這會顯示出檔案被回復的程度,並符合下面所介紹的「檔案狀態圖示」“file status icons”. 點擊_「狀態」“Status”_來把被刪除的檔案依照三種基本分類整理,其分別是_「優良」“Excellent”_、_「無法回復」“Unrecoverable”_.**「註記」“Comment”:**這會顯示為何某個檔案可能可以或無法回復,以及其檔案在「Windows 主檔案表」“Windows Master File Table”上被覆寫的程度.點擊_「註記」“Comment”_ 以檢視某一檔案已被覆寫的程度.  
每一個檔案都有一個以顏色表示的狀態圖示，其顯現出其可否被成功回復的程度:下面解釋每一個狀態圖示的意思:綠色: 其完全回復的機會最高；橙色:其回復機率在可接受範圍。紅色:其回復機率很低.  
  
**3.2「如何不透過Recuva精靈來執行描掃」“How to Perform a Scan without Using the Recuva Wizard”**  
要直接使用Recuva　主畫面, (意即, 不使用_Recuva精靈_), 請執行以下步驟:  
**第1步.**直接點擊 Recuva圖示或是從 Start > Programs > Recuva > 開啟Recuva.  
**第2步.** 勾選_「啟動不要顯示精靈」"Do not show this Wizard on startup"_選項, 然後點擊「取消」“Cancel”將出現以下畫面:![](http://self.jxtsai.info/tool_recuva7.png)主畫面_Piriform Recuva_會分成左側的結果面版以及_「預覧」“Preview”_, _「資訊」“Info”_和_「首部」“Header“_分頁，其用來整理與檢視刪除檔案的資訊.這裏可以設定某些掃描選項,有點類似_Recuva 精靈_.  
**第3步.**點擊下拉式清單後再選擇要掃描的磁區;_「本地磁碟」“Local Disk (C:)”_是軟體的預設，本練習中顯示如下:![](http://self.jxtsai.info/tool_recuva8.png)

_「檔名」“Filename”_或_「路徑」“path”_的下拉式選單可以指定要找的檔案類型, 它有點像是_Recuva 精靈中的檔案類型 File type_ 畫面.![](http://self.jxtsai.info/tool_recuva9.png)  
_「檔案名稱」“Filename”_或_「路徑」“path”_特性有文字框與下拉式選單旳組合. 這主要有二種用法: 讓你直接搜㝷某特定檔案, 或是用來被刪除檔案的清單與其檔案類型進行整理.  
另一個用法是, _「檔案名稱」“Filename”_或_「路徑」“path”_用於搜㝷特定檔案類型之檔案,或是透過結果面版中的來整理一般性被刪除檔案清單.  
  
要開始掃描找到一個已知其全名或部份名稱的檔案, 執行下面步驟:  
**第1步.** 如下輸入要回覆的檔案名稱(本例中,該檔案_triangle.png_ 被掃描):![](http://self.jxtsai.info/tool_recuva10.png)**竅門:**點擊“X”以重新設定_檔案名稱和路徑_ (其將會顯示為淡灰色).  
**第2步.** 點擊「掃描」“Scan”開始找你所刪除的檔案; 一會過後,將會出現如下的畫面:![](http://self.jxtsai.info/tool_recuva11.png)  
  
**3.3 如何使用Recuva進行深度掃描**  
_「啟動深度掃描」“Enable Deep Scan”_選項可讓你執行更完整的掃描;當然這樣也得花上更多的時間, 得視電腦速度以及多少檔案而定.如果你初次的掃描沒有顯示出要回復的被刪除檔案後，這個功能也許能派上用場.雖然深度掃描可能會花上幾個小時，但它可以提高回復檔案的機率.Recuva _「深度掃描」“Deep Scan”_可透過在_Recuva 精靈_下在勾選_「啟用深度掃描」“Enable Deep Scan”_選項 .  
**第1步.** 點擊「選項」“Options”，會進入 _「選項」“Options”_畫面, 然後點點_「動作」“Actions”_分頁如下圖:![](http://self.jxtsai.info/tool_recuva12.png)  
**第2步.**勾選_「深度掃描」“Deep Scan”(增加掃描時間)_, 然後點擊「確認」“OK”.  
**第3步.** 點擊「掃描」“Scan”執行_「深度掃描」“Deep Scan”_功能.稍早提過,深度掃描要花上數小時之久，端賴電腦速度及檔案數量而定:![](http://self.jxtsai.info/tool_recuva13.png)  
  
**3.4 介紹選項介面**  
這部份,將介紹如何使用_「選項」“Options”_介面不同的設定，以成功地回復或覆寫私密敏感檔案. 要理解這些設定,請執行以下步驟:  
**第1步:** 點擊「選項」”Options“後會進入如下的畫面:![](http://self.jxtsai.info/tool_recuva14.png)  
_「選項」“Options”_介面分成_「一般」“General”_, _「行動」“Actions”_以及_「關於」“About”_三個分頁：_「一般」“General”_分頁可以定義一些重要的設定, 包括_「語言」“Language”_ (Recuva 支援37種語言), _「檢視模式」“View mode”_以及取消或啟用 _Recuva 精靈_.![](http://self.jxtsai.info/tool_recuva15.png)

檢視模式可以選擇要如何來觀看被刪除的檔案,當_Piriform Recuva_之下用滑鼠右鍵點擊某個檔案時也能啟動此功能.**「清單」“List”:**可以以清單形式來檢視被刪除的檔案**「樹狀」“Tree”:**可以用目錄路徑結構來檢視被刪除的檔案.**「縮圖」“Thumbnails”:** 以縮圖形式來檢示被刪除的檔案.  
其中最重要的可能是, _在_「一般」“General”_ 分頁下的「進階」“Advanced”_部份可設定資料可以被隨機覆寫的次數，這樣可以防止被對手或惡意者企圖來回復被刪除的檔案.  
_「安全覆寫」“Secure overwriting”_下拉式選單顯示出四種覆寫方式.預設的方式是_「簡單覆寫」“Simple Overwrite (1 pass)”_. 一次表示相關文件、檔案或目錄將會被隨機資料覆蓋的次數，其無法再回收讀取.  
**第2步: 選擇**_“DOD 5220.22-M (3 passes)”_如下:  
![](http://self.jxtsai.info/tool_recuva16.png)  
對文件檔案等進行一次覆蓋動作應可以有效地安全刪除檔案，但仍有些資源能力的當事人可以試著回復一些相對簡易被覆寫的檔案.而三次覆寫則是時間與安全之間權衡的最佳選擇.  
**第3步.**點擊「確認」“OK”以儲存_「一般」“General”_分頁設定選項.![](http://self.jxtsai.info/tool_recuva17.png)**「顯示隱藏的系統目錄」“Show files found in hidden system directories”:**該選項可以讓你顯示系統下示隱藏的目錄和檔案.**「顯示無位元檔案」“Show zero-byte files”:** 這個選項可顯視那些沒有內容或幾乎不佔空間且基本上是不可回復的檔案.「顯示安全刪除的檔案」“Show securely deleted files”: 這可以在結果」面版顯示剛才所安全刪除的檔案.  
**注意:**如果你已用CCleaner或其它類似軟體, 當要安全刪除檔案時，因安全考量請改變檔案名稱成為像ZZZZZZZ.ZZZ**「深度掃描」“Deep Scan”:** 可以掃描整個磁碟來找出被刪除的文件或檔案; 如果之前的掃描無法有效地找到原檔案位置,深度掃描也許有用，但也得花上更多時間.請參考3.3部份「如何用Recuva執行深度掃描」.**「掃描非刪除檔案」“Scan for non-deleted files” (回復毀壞硬碟或是重新格式化硬碟):**其試著回復遭到物理毀壞或軟體破壞的硬磁._「關於」“About”_分頁顯示軟體版本資訊,以及Piriform 官網連結.現在你應該比較知道如何在選項介面下的_「一般」“General”_與 _「行動」”Actions“_分頁裏設定不同的掃描功能, 也已經知道如何實際地回復或安全地覆寫要刪除的敏感私密檔案.  
  
**如何使用Recuva回復與安全地覆寫檔案  
4.0 開始之前**  
在這部份,你將學到如何回復之前被刪除的檔案,以及如何安全地刪除任何敏感機密的資訊.Recuva可創建一個全新的目錄來存放所回復的檔案資料. 雖然你也可以使用現有的目錄,但因安全和保安之故,建議最好還是將回復的檔案放在可卸除式的移動裝置，如USB或備份磁碟.**Important重要:**雖然Recuva是一套優秀的安全覆寫工具,但它可能還是會留下檔案標記顯示出檔案的存在. 為保護隱私和安全,最好把私密敏感的資料存在可卸除的移動裝置上,不要留下原始的位置或路徑資訊.  
  
**4.1 如何回復被刪除的檔案**  
要回復已遭刪除的檔案,請執行以下步驟:  
**第1步.**接上移動式儲存裝置到電腦上.  
**第2步.** 勾選要回復的檔案以便啟動回復鍵，或是雙擊該檔案以選取並反白之.  
**第3步.**點擊「回復」“Recover”以進入_「瀏覧」目錄“Browse For Folder”_畫面.  
**第4步.**選擇目地的後，點擊「新增目錄」“Make New Folder”功能以創建回復檔案的資料夾，其顯示如下.![](http://self.jxtsai.info/tool_recuva18.png)**注意:**在本示範案例中,儲存回復文件的目錄被賦予一個明顯的標籤.然而在現實生活中, 要保持資訊的機密和安全,應當要小心留意註記標籤的方式.  
**第5步.**點擊「確認」“Yes”開始回復程序; 此時會出現如下畫面的進度條:![](http://self.jxtsai.info/tool_recuva19.png)當檔案完成回復後,將出現一個確認畫面如下圖:![](http://self.jxtsai.info/tool_recuva20.png)**注意:** Recuva支援多檔案回復功能.只要勾選多個欲回復的檔案，並依照步驟**3**到**5**的程序來執行即可.現在你已學會了如何回復檔案方式，接下來我們來看看如何使用彈出選單來執行多檔案的回復與安全覆檔案方式.  
  
**4.2 如何使用彈出選單**  
Recuva 提供不同方式來選擇文件、檔案或目錄.**「勾選」“Checking”** 是最常用來快速選取多個非連續或個別檔案的方法.**「高亮」“Highlighting”**則適合於快速選取多個連續的檔案或群組.主畫面下用滑鼠右鍵來點擊已被刪除的檔案以啟動如下圖的彈出式選單:![](http://self.jxtsai.info/tool_recuva21.png)**「回復高亮的檔案」“Recover Highlighted”:** 回復所選取的高亮已刪除檔案.**「回復勾選檔案」“Recover Checked”:**回復所勾選的已刪除檔案.**「勾選高亮」“Check Highlighted”:**可勾選其中某高亮的被刪除檔案.**「取消勾選高亮檔案」“Uncheck Highlighted”:**取消勾選其中某高亮的被刪除檔案.還記得_「一般」“General”_分頁下的_「選單」“Options”_中可以設定檢視的畫面吧. 它可以選擇檢視被刪除檔案的方式.**「清單」“List”:** 以清單方式來檢視被刪除的檔案，如圖表5**「樹狀」“Tree”:**以樹枝延伸形式來檢視被刪除檔案之路徑與目錄.  
**「縮圖」“Thumbnails”:**以縮圖方式來檢視被刪除的檔案.**「高亮目錄」“Highlight Folder”:**可依目錄路徑，選取多個被刪除的檔案,並可讓你執行彈出選單中的動作.**「安全覆寫高亮」“Secure Overwrite Highlighted”:** 安全地覆寫過被選取的高亮刪除檔案.**「安全覆寫勾選」“Secure Overwrite Checked”:** 安全地覆寫某個被勾選的刪除檔案,以改變其狀態圖示轉為紅色.  
  
**4.3 如何安全地覆寫一個被刪除的檔案**  
要安全地覆寫一個被刪除的檔案,請依下列步驟:  
**第1步.** 勾選要進行全地覆寫的某個檔案後, 用滑鼠右鍵點擊勾選框以啟動彈出式選單.  
**第2步.** 選取「安全覆寫勾選」“Secure Overwrite Checked”後會出現下面的確認對話框:![](http://self.jxtsai.info/tool_recuva22.png)  
**第3步.**點擊「確認」“ ”Yes“開始覆寫過程;其時間視檔案大小、狀態以及 depending on the size and status of the file as well as the _「「安全覆寫」”Secure overwriting“_選擇的方式而定. 覆寫程序完成後,會出現以下畫面:![](http://self.jxtsai.info/tool_recuva23.png)你已成功地利用Recuva 完成了回復或安全覆寫檔案.  
  
**5 隨身版的RECUVA  
5.1 安裝版與隨身版Recuva的差異**  
隨身版工具並不是安裝在本地的電腦上,故其存在與使用並不會被偵測到.但還是要記住, 外部連結的儲存裝置、USB記憶卡或是隨身工具只有在自己的電腦上使用才安全,若接觸許電腦恐怕會曝露在廣告軟體、間諜軟體、惡意軟體或病毒感染等風險.

除此之外，隨身版與安裝版之間並無別的差異.  
  
**5.2 如何下載和解壓縮隨身行動版的Recuva**  
下載和解壓縮隨身行動版的Recuva,請參照以下步驟:  
**第1步.** 直接點擊[http://www.piriform.com/recuva/download/portable](http://www.piriform.com/recuva/download/portable)網頁上合適的隨身版檔案,接下來會出現以下畫面:  
**第2步.**點擊「確認」“OK”以儲存檔案_rcsetup140.zip_.  
**第3.** 用滑鼠右鍵點擊該檔案以啟動彈出式選單,然後選取「壓縮檔案」，其圖示如下:![](http://self.jxtsai.info/tool_recuva24.png)  
**第4步.**引導至移動裝置或 USB 記錄卡, 然後點擊「新目錄」來創建一個新目錄以存放解壓縮過後的安裝檔案，其如下圖.![](http://self.jxtsai.info/tool_recuva25.png)  
**第5步.**輸入目錄名稱 :![](http://self.jxtsai.info/tool_recuva26.png)或者, 你可以在下拉式選單中打入目錄名稱:![](http://self.jxtsai.info/tool_recuva27.png)**注意:** 本示範案例中,新目錄名稱叫作 「Recuva Portable」,使用者當然可以另取其它名稱.  
**第6步.**點擊「確認」“OK”開始解壓縮其內容到剛才新建的資料夾中.  
**第7.**引導到目的地的移動式儲存裝置或USB隨身碟當中,如下圖所示,然後打開目錄確認檔案有成功地放在此資料夾內.![](http://self.jxtsai.info/tool_recuva28.png)  
**第8步.** 雙擊檔案_Recuva.exe_即會啟動隨身版Recuva 精靈.相關操作請直接參考前面Recuva工具指南之介紹來進行設定與使用.

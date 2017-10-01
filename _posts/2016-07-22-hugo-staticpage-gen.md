---
author: jx tsai
comments: true
date: 2016-07-22 16:57:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/07/22/%e8%a9%a6%e7%94%a8hugo-%e6%9c%ac%e6%a9%9f%e5%ae%89%e8%a3%9d%e7%af%87/
slug: '%e8%a9%a6%e7%94%a8hugo-%e6%9c%ac%e6%a9%9f%e5%ae%89%e8%a3%9d%e7%af%87'
title: 試用hugo -- 本機安裝篇
wordpress_id: 46
categories:
- blogging
- git
- opensources
---

之前知道github有提網頁寄存功能[GitHub Pages](https://pages.github.com/)(其主要目的是為了讓在其上寄居的開發者可以透過此服務來介紹他們放在github上面的公開專案),便依樣學樣地新增一個資源庫作為存放個人在github 的靜態網頁。一開始放入的是自己在free code camp的網頁前端學習的小專題----個人自我介紹網頁，其透過codepen.io可以無痛地把它轉入到GitHub Pages。後來看GitHub Pages網站的介紹，一度試著在自己的電腦上安裝Jekyll（[參見當時記下的試驗筆記](http://self.jxtsai.info/2016/04/jekyll.html)），雖然可以在電腦端成功地建立Jekyll，但不知為何一直無法順利地把本機裏的文章成功同步到GitHub Pages上面，故在安裝筆記後就沒什麼下文 （ノ＿　＿）ノ▽。  
這兩天看到有人用的是另一種以go寫成的靜態網頁産生器[Hugo](https://gohugo.io/)架個人網站,便好奇前往Hugo官網探探究竟，其介紹影片大膽宣稱可以在二分鐘之內就架好一個網站，便好奇地依樣試著操作一下。嗯，如果是在本機上安裝，的確輕快無痛。但後期的模版挑選、樣式修改以及上傳到github當然就不只這個時間了（大部份原因也是我仍然對於git指令操作不熟）。本文以中文記下自己如何在電腦上安裝Hugo<strike>與成功上傳到github　page的</strike>使用筆記。  
  
１） Hugo軟體介紹與優勢  
在Hugo蒐頁上強調此軟體的特色就是「快」「簡單」。不像過去網站內容管理軟體得依賴伺服器、資料庫、解析器等配合。從其官網上的介紹，所謂靜態型網頁static site，不同於過去大多數的網頁內容管理軟體（如wordpress, durpal等等）其動態性就是每當有一名訪者，網站伺服器系統就得接收其請求而作變動，這也就相對地要耗費伺服器效記憶、CPU效能，以及寫文章、讀網頁時花上的等待動態網頁內容新建時間（雖然隨著電腦效能的提高與網路頻寛的加大，時間早已大幅縮短,也有利用緩存cache設計來「快取」html動態內容）。為了節省時間，Hugo則是先利用本機上進行內容的撰寫與網站架構編排設計後，再把它佈署到網路上。也就是說Hugo先安裝在自己的電腦上，其帶有伺服器作用啟動時會把所撰寫的文件轉換成html格式，也可以在編完後很輕鬆地發佈到網路上。  
[![](https://1.bp.blogspot.com/-ID-kC9nG30Y/V5I1vgFizdI/AAAAAAAAKiM/uEhYFM4gZjAMwyQn9stPJFjxJq0IZCqegCLcB/s1600/hugo.png)](https://gohugo.io/)  
  
2） 本機電腦端安裝  
先到其[資源庫下載](https://github.com/spf13/hugo/releases)符合自己電腦作業環境的軟體包，當然是跨（linux, apple, windows）平台的支援。以我lenovo x200 unbuntu 14.04 64bit為例，下載hugo_0.16-1_amd64.deb 這個檔案（不到3M）,透過安裝ubuntu software center解壓安裝，打開ubuntu software center大概是安裝過程最花時間的一個步驟吧。  
![](https://4.bp.blogspot.com/-iXqp5Cmd5IA/V5Ib4G9GEeI/AAAAAAAAKhA/9phB-_26XAokvPDmVfINoSn-x62CtW1awCLcB/s1600/software%2Bcenter.png)  
  
安裝完成後，打開端終機文字指令，輸入  
$hugo version ##可以看目前的版本。  
$hugo help  ##主要指令整理   
$hugo new site myhugo ##利用hugo新建一個網站，紅字為新站（專案）名稱，在本例中即為myhugo  
秒殺之間，一個新網站資料架構就在自己的電腦上自動産生了。在剛剛文字指令的現有目錄下，發現出現一個新的資料夾「myhugo」, 且底下還有五六個資料夾與一個config.toml檔案。  
![](https://1.bp.blogspot.com/-wQDK_EutVLo/V5Ic56FKHvI/AAAAAAAAKhM/ozaYyATenoUZAKGbHaKTXmgkBy4HNxtpgCLcB/s1600/myhugo.png)  
當然目前這個新站中內容還是一片空白，其文章將會放在/myhugo/content/ 底下，若要新增一篇文章，其指令為：(記得要先把端終機的工作目錄切換到新專案下)  
$hugo new post/first-post.md ##從副檔名可知其以[markdown語法](http://markdown.tw/)進行文章編寫。  
下了新增一篇文章的指令後，隨即發現在在/myhugo/content/底下多出了/post/first-post.md的資料夾與檔案，其可以一般文字編輯軟體(如sublime text,gedit, notepad等 )進行內容撰寫  
![](https://3.bp.blogspot.com/-I5uLUGYvtHQ/V5IehL3ntsI/AAAAAAAAKhY/gd2txHYSqrkOwoQz7HDK-W54FX4iHfQOACLcB/s1600/sublime.png)  
![](https://4.bp.blogspot.com/-gl5byUZzT20/V5I9oLmPjII/AAAAAAAAKic/mgdN0sGP3UIVaJJQvsBjhP7yg70L8gpbgCLcB/s1600/edited.png)  
從first-post.md檔案的原始內容，不難猜出+++之間為文章基本資訊，如産生日期、篇名，文章狀態等+++，至於內文則是從第二個+++以下開始寫起即可，按照的語法規則為markdown格式。文章寫完儲存，接下來就是要測試看看它在本機電腦瀏覧器端的呈現情況如何，要啟動hugo 伺服器執行命令，只要在新建專案下，打下文字指令：  
$hugo server ##它會預留埠部1333作為伺服器網頁串接對應口，故可用瀏覧器開啟新專案網站下的內容（http://localhost:1333）  
但此時打入此網址，卻是什麼內容也看不到。這是因為伺服器串連雖然開啟了，但是/myhugo/content/post/底下的文章還是草稿狀態，必須下指令把草稿變成伺服器可接收的狀態。故需得再下一串指令：  
$ hugo server --buildDrafts #其實自己手動，在打完文章後，把最上面++draft = "true" 改成“false”+++ 即文章狀態原來的草稿變成了“不是草稿”的狀態，也具有同樣的效果。   
![](https://4.bp.blogspot.com/-RLyUn31lPho/V5IhvvplrFI/AAAAAAAAKhk/AJfG0UFfIZUoL6C_S4iMjY4IelX52V31gCLcB/s1600/server.png)  
這時候再試看看在瀏覧器打入http://localhost:1333　網址，哈還是空無一物(。_。)，因為還未設定網站主題外觀啦(所「themes」目錄夾下空空如也）。可到[gohugo官網上挑選喜歡的主題外觀](https://themes.gohugo.io/)，並下載到「themes」資料夾（或是直接以git方式抓回「themes」,當然前提是電腦有裝git）  
  
假設我在主題目錄新增了「hugo_theme_robust」這個主題佈景，則下的指令為  
$ hugo server --theme=hugo_theme_robust  
這時瀏覧器再開啟http://localhost:1333，竳楞竳楞竳楞O口O!,一個網站初步模樣就作出來了  
![](https://3.bp.blogspot.com/-oT69XRjCiyQ/V5IlCvXn2FI/AAAAAAAAKhw/WSJePBFGTEgPosVLgXIMR1kiHYbwDv5EwCLcB/s1600/fist%2Bpost.png)   
當然接下來還是得版面圖片作不少細部的調整安排、整合加入disqus外掛（好讓靜態文章能産生讓讀者回應留言的功能）、config.toml設定檔的更新等等。  
![](https://4.bp.blogspot.com/-rbC5EFKAnRE/V5IopphSPsI/AAAAAAAAKh8/qGBnYesyceE0rG-oZaAmrrNqvqh1SnMiACLcB/s1600/config.png)  
目前我還沒深入研究自定主題版面的調校，不過如果要在文章中加入圖片，其作法是：在新專案目錄下的「static」新增一個「images」資料夾，然後把圖片丟到下面。然後在文章中加一行image = "XXXXXXX.jpg"（XXXXXXX.jpg為放入到/static/images/底下的圖片檔名稱）  
  
根據Hugo官網操作教學手冊，它可以佈署在github pages, gitlab, bitbucket（arobatic）等支援靜態網存放的空間。我已成功佈置到github pages, 另外兩個還沒試，詳情待下文分解好了。  


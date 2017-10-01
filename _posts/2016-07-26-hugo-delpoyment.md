---
author: jx tsai
comments: true
date: 2016-07-26 03:17:00+00:00
title: 試用hugo -- 網路佈署篇
wordpress_id: 44
categories:
- blogging
- git
---

前面已經寫下如何[在本地端的電腦上安裝好Hugo](http://self.jxtsai.info/2016/07/hugo.html)並學習使用markdown語法快速地建置一個網站專案，接下來就是探討如何把本機電腦上編好的文章與網頁發佈到網路。Hugo本身官網介紹網路佈置方式提到，它可以使用「傳統的」（這是我自己加的）FTP、SFTP方式傳檔，也可以支援git push、WebDAV等方式。故首先示範一下傳統的FTP檔案上傳法。  
1) FTP/SFTP上傳  
當然檔案上傳不是把 hugo new site底下的資料目錄夾丢上網路空間，而是在hugo網站網頁的專案目錄夾底先下一道文字指令  
$hugo --theme=hugo_theme_robust （指令hugo就是啟動網站內容生成的關鍵字，這裏沒有加「server」字眼，就是沒必要啟動本機電腦的伺服器<strike>模擬</strike>功能，hugo_theme_robust為指定要使用的主題佈題，當然也可以指定其它已裝在同一層目錄/themes/ 其它的佈景主題）  
下了這個指令後，在該專案的目錄下會發現多了「public」的資料夾，這是hugo把新網站專案自動轉成了css, html等網頁語法與網站架構，原則上這個資料夾底下的東西，就是我們欲公開放到網路上供他人閱讀交流的資訊內容。  
不過在下這個産生public資料夾的關鍵指令之前，別忘了要先修改config.toml這支檔案當中的baseurl資訊，也就把放置資料的網址位置填進去,這樣在執行hugo關鍵指令自動産生public內容時相應的連結位置才會正確。  
![](https://4.bp.blogspot.com/-lxK1GgMVWaQ/V5NZ1bOykCI/AAAAAAAAKjg/sdZTIHAGtrwWgtTVBK4xV_Kl7nfQlTfWACLcB/s1600/config.png)  
打開ftp軟體，然後把public底下的東西一股腦地丢上指定位置的資料夾。因為檔案都蠻輕小的，很快就完成了上傳手續。  
![](https://4.bp.blogspot.com/-J3fI36Z2Tsk/V5NalvSAlCI/AAAAAAAAKjk/zuNYjlpyOAM6NRKVQ5ljsOVXkyKzv3XTACLcB/s1600/ftp.png)  
用瀏覧器開啟自已所指定放置hugo生成的「public」資料網址（本例中為：http://jxtsai.info/blog/second/），果然就看到一個以hugo為平台的新網頁專案完成了。  
![](https://2.bp.blogspot.com/-Cmy4R0zUKx8/V5NbwSSEABI/AAAAAAAAKjs/EAPUKRbHLHIjWHzllD7zQ4WLdLyMSS73gCLcB/s1600/myhugo.png)  
  
2）git push  
嗯，前面Ｈugo的介紹演示，感覺它是一個又酷又潮的網站內容産生器新玩意。但是居然用FTP這種「老掉牙的手工方式」來更新，實在有點遜耶( ▔___▔)y-～ 。所以接下來要學點讓自己看起來比較geeky,nerdy比較有點技術質地的網頁佈署方式--git push。 Hugo 示範教學中演示了三個以git版本控制提供代碼管理的網路服務商----github、gitlab、Bitbucket支援，三者都同時有提供靜態網頁寄存的服務（static pages），其中又以第一家最為知名，用戶人數最多。  
i）github.io 寄存  
pages.github.com之所以提供靜態網頁，主要是為了讓會員除了在它的服務平台上寄放代碼程式庫外，再提供網頁空間讓代碼開發者，公民技客或新創公司能介紹它們的專案或服務內容。所以要把網頁網站託管在github，首先要有github帳號，並新建一個名稱為「username.github.io」的專案Repository,其中username為自己github帳號，一定要取這樣的資源庫名稱才能正確串接github page.(以為我例，github username為jxtsai,故專案名為「jxtsai.github.io」,基本上這樣https://jxtsai.github.io 就是自己在github上託管的網頁網址，其亦提供自定DNS服務，不過此不在本文記述範圍)  
回到自已電腦上的hugo網站專案工作目錄下，和前述的FTP方式一樣，先修改config.toml這支檔案中的baseurl資訊，調整成為username.github.io。以我自已個人github帳號為例，打算把用hugo新建的網站專案放在一個名為murmur的repository底下，故baseurl="https://jxtsai.github.io/murmur/"  
![](https://1.bp.blogspot.com/-QxySTBRyP0o/V5Yw69WFVwI/AAAAAAAAKlI/Q3n8S3F84JQMn8K-DLLkiCQ3Yf-lDP_FgCLcB/s1600/githubpages.png)  
與前述ＦＴＰ上傳準備相同，在hugo頁專案目錄底下一道文字指令  
$hugo --theme=hugo_theme_robust （hugo_theme_robust為指定要使用的主題佈題，當然也可以指定其它已裝在同一層目錄/themes/ 其它的佈景主題），該專案目錄下會發現多了「public」的資料夾  
在本機電腦上另外新增一個資料夾（假設取名為murmur），它是準備用來存放要推到github的公開資料,把剛才新生成的「public」內容複制到這個新增資料夾下。另外在github網站上再新建一個Repository，其名稱要與config.toml檔案裏的baseurl資訊相一致。  
為電腦上外新增一個資料夾murmur在其底下進行git 初始化與串連github reposity設定  
~/murmur$git init ##該指令為資料夾murmur進行git 初始化,使之成為本地端數據庫  
~/murmur$git remote add origin https://github.com/jxtsai/murmur.git ##串連遠端github上的murur repository  
~/murmur$git checkout -b gh-pages ## 切換到遠端「username.github.io」數據庫的分支gh-pages，這是github用作專案網頁發佈的分支指定名稱。  
~/murmur$git add --all ## 將目錄下所有的檔案加入到git版本控制索引  
~/murmur$git commit -am "initial commit"　##準備提交檔案，執行commi命令提交, 雙引號間為個人加註的訊息  
~/murmur$git push origin gh-pages ##把電腦端murmur 底下的檔案透過gh-pages分支方式推上了murur repository  
如果沒出現錯誤訊息成功把/murmur/底下的檔案都推上了githhub,那麼用瀏覧器打開網址:https://jxtsai.github.io/murmur,就可以看到用Hugo作成的網站已順利佈署在github上面囉‧★,:*:‧(￣▽￣)/‧:*‧°★*  
![](https://1.bp.blogspot.com/-uxjzoRmGUiQ/V5RbHAdor4I/AAAAAAAAKkQ/3PiTDLxAfGYexv_7A9bEfUt3TZDRso7KgCEw/s1600/hugo.png)  
  
ii)<strike>gitlab</strike>：目前仍未成功。  
  
iii) bitbucket  
bitbucket.org 也是一家提供開發者（公司）源碼代管與雲端佈署的服務商，為了測試hugo，我初次註冊試用它的服務。如何透過bitbucket與aerobatic資源庫與靜態網頁互相整合的服務來佈置hugo，其實官網上介紹得蠻清楚 [deployment with Bitbucket & Aerobatic](http://gohugo.io/tutorials/hosting-on-bitbucket/#continuous-deployment-with-bitbucket-aerobatic)  
把端終機的工作目錄切到新建的hugo網站專案工作目錄下，並生成一個「package.json」檔案，其檔案內容為：  


<blockquote>{  
"_aerobatic": {  
"build": {  
"engine": "hugo",  
"themeRepo": "https://github.com/alexurquhart/hugo-geo.git"  
}  
}  
}  
</blockquote>

##其中themeRepo": "https://github.com/alexurquhart/hugo-geo.git“ 指定主題背景為alexurquhart，當然也可以換成其它。  
  
在遠端bitbucket.org上新增一個專案資源庫repository(假設命名為myhugo), 然後把本機端的hugo網站專案整個資料夾與遠端 myhugo repository 進行串連。  
$git init  ## 將hugo網站專案資料夾初始化,使之成為本地端數據庫  
$echo "/public" >> .gitignore ## 讓git自動忽略「public」資料夾。  
$git commit add . ##新增提交檔案， 「add .」其中點表示提交資料夾下所有檔案  
$git commit -m "Initial commit"## 準備提交檔案，執行commi命令提交, 雙引號間為個人加註的訊息  
$git remote add origin git@bitbucket.org:YourUsername/myhugo.git  
$git push -u origin master ##把本地端檔案推上myhugo repository  
  
這裏和i)github有點不一樣的是，github的佈置要先在本機端執行關鍵字以産生一個「public」的資料夾，然後把「public」底下的東西push上github pages。但是在bitbucket/gitlab的佈署，則是把hugo網站專案整個資料夾都push上去遠端資源庫，還下指令叫git忽略「public」不要推上去。另外在這裏也完全不用動到config.toml這支檔案的修改。從bitbucket查看推上去的代碼，也和本機端的資料夾目錄與內容不相同，嗯這是什麼原因我也還搞不清楚(￣３￣)a。  
把本機端hugo網站專案推上bitbucket.org repository之後，還要進行Aerobatic的安裝設定。[Aerobatic](https://www.aerobatic.com/)是一個提供靜態網頁git push的服務商，bitbucket.org有提供許多源碼專案的外掛延伸套件，Aerobatic hosting 就是其中之一。這些外掛套件可以在repository/Setting/Integrations/Services 找到。成功把檔案推上bitbucket後，hugo專案需新增Aerobatic hosting套件。接下來的設定動作算是蠻直觀的，成功後就可以在https://jxtsai.aerobatic.io/ 看到自己用hugo作的新網站了。  
  
![](https://4.bp.blogspot.com/-jD90l6mh-KE/V5TOQt4mhYI/AAAAAAAAKkk/vlXFtqHAzqERSx7KjSJL0WPBikNlBRBowCLcB/s1600/aerobatic.png)  
![](https://2.bp.blogspot.com/-c3sXA8xGpE8/V5TOKmXOvjI/AAAAAAAAKkg/dGv1ByNbd1gR0-D7mclNxhb953Gz4klBQCLcB/s1600/deploy.png)  
![](https://2.bp.blogspot.com/-A82pDvBYkcI/V5TOXVIv3FI/AAAAAAAAKko/V0OnrLW1kSwAznBHEPU1f7vzXs70_mEKgCLcB/s1600/Screenshot%2Bfrom%2B2016-07-24%2B21%253A35%253A33.png)  
![](https://2.bp.blogspot.com/-1z6RFNKI0sg/V5TPr6XKWgI/AAAAAAAAKk0/K7HhSWWLVkwY0kQAZ2XthSlhE-G4G5tCgCLcB/s1600/Screenshot%2Bfrom%2B2016-07-24%2B21%253A35%253A13.png)  
  
心得：Hugo專案的開發者表示，自己原本是用wordpress，但覺得透過瀏覧器在線寫東西很麻煩（耗時），有安全顧慮又不喜歡html複雜的語法，所以決心開發新的靜態網頁生成軟體。我自己這兩三天來在電腦上使用與網路佈置的感想，比起用ruby, python寫成的網頁架構webframework,還得裝伺服器軟體、作資料庫連接，它真的是一個敏捷輕巧的網站快速製作神器。但要更細緻地了解其CSS、網頁內容架構當然得投入不少時間研究才能調配出一個賞心的網站。對於許多技術取向的開發者而言，隨時把筆記資料存在自己的電腦上，更佳支援程式碼示範的MD語法、清爽直觀的網頁版面、敏捷自主的網路發佈更新，或許更符合新一代程式開發者的偏好。以我個人的習慣而言，這一年多來較常更新網誌，直接把草稿打在wordpress, blogger上面也沒覺得有什麼不好，因為我本來就不是什麼技術取向的技客ლ(ﾟдﾟლ)。日後若想試著多熟練markdown語法以及git基本操作指令，倒是可以考慮偶而用它來寫作吧。  


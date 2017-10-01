---
author: jx tsai
comments: true
date: 2016-04-26 14:33:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/04/26/jekyll-%e4%bd%bf%e7%94%a8%ef%bc%88%e6%9c%ac%e6%a9%9f%e5%ae%89%e8%a3%9d%e7%ad%86%e8%a8%98%ef%bc%89/
slug: jekyll-%e4%bd%bf%e7%94%a8%ef%bc%88%e6%9c%ac%e6%a9%9f%e5%ae%89%e8%a3%9d%e7%ad%86%e8%a8%98%ef%bc%89
title: jekyll 使用（本機安裝筆記）
wordpress_id: 84
categories:
- blogging
- git
- python
- ruby
---

因為在 github 上面看到它有支援「[靜態網頁](https://github.io/)」，讓使用者透過該功能更簡單清楚地介紹自己投入的相關開源專案，我也就依樣畫葫蘆地申請了其空間，並透過git工具把自己依freecodecamp 要求透過[codepen.io](https://codepen.io/)練習的小作業---[個人介紹網頁](https://jxtsai.github.io/)，同步上傳到其中。(好啦，我的ＨＴＭＬ，ＣＳＳ以及整體設計美感很糟)  
  
後來看到github pages還推薦用戶不妨可以安裝[jekyll](https://jekyllrb.com/)來作為本地端的網頁或部落格撰寫工具，因此就嘗試了一下如何使用，本文即是這場實驗練習的心得筆記。  
  
這裏有所謂[快速安裝設定指南](https://jekyllrb.com/docs/quickstart/),但前提是你的電腦要符合以下設置環境的五大條件：  
  
*Linux, Unix, or Mac OS X  
聽說在windows作業環境下安裝ruby有點麻煩，但幸好我可以輕鬆地跳過這關。  
  
*Ruby (including development headers, v1.9.3 or above for Jekyll 2 and v2 or above for Jekyll 3)  
我目前使用的ubuntu 14.04作業系統似乎就有預裝了ruby，但其版本是1.7還是1.9，不符合jekyll要求的ruby2.0以下環境。因為ubuntu官方列出的軟體包支援並未把ruby2.0放在其上，所以如果只用apt-get update， apt-get install 也不用把ruby更新到2.0以上的版本。  
作法是參考[這篇把ruby資源庫加入到軟體更新記錄器](https://www.brightbox.com/blog/2016/01/06/ruby-2-3-ubuntu-packages/)中，再來安裝好 ruby2.3.0的版本。安裝好後，可以透過文字命令列檢查目前機器上的ruby 版本（$ruby -v，　下一行出現$ruby2.3.0)  
不過我遇上的問題是，不了解ruby 不知道其實目前電腦上同時安裝了二個版本的ruby  
（可在文字命令列打上$ruby-switch --list），它會列出電腦上安裝的版本，因此即便我自以為下載安裝符合要求的最新版本，但是機器在運行的仍然是1.9版本，故在後面安裝rubygems時，一直出現錯誤訊息。  
那麼要如何把電腦轉設使用ruby 2.3呢？　很簡單，只要在文字命列打入（$sudo ruby-switch --set ruby2.3.0），接下來就可以順利安裝rubygems以及jekyll   
  
*RubyGems  
注意上一段文字，關於使用中的ruby 版本問題，我就是一度卡在這裏，造成RubyGems安裝版本一直出錯  
  
*NodeJS, or another JavaScript runtime (Jekyll 2 and earlier, for CoffeeScript support).  
依其官網上的說明指示，https://nodejs.org/en/download/package-manager/，還蠻容易安裝好nodeJS。  
要啟動nodeJS，只要在文字命令上打入（$node）網頁伺服器的功能就可以開始運作  
  
*Python 2.7 (for Jekyll 2 and earlier)  
一般linux 的作業環境，似乎都有預裝python了吧？  
  
當檢查好電腦系統環境已皆備上述條件後，就可以進入安裝jykell的手續。至於安裝的方式，其實很簡單，只要在文字命令列打入（$gem install jekyll）照理說就是自動安裝好jekyll。這時候你就可以利用jekyll新增某一個資料,作為你電腦這端靜態網頁資料存放的位置。例如我下一個指令：$jekyll new blog, jekyll就會在當前位置下，新增出一個「blog」資料夾。只要把文字命令列移置「blog」之下，再打入指令：　$jekyll serve（當然要記得開啟nodeJS運行），這時候它就會告訴你打開瀏覧器http://localhost:4000(127.0.0.1:4000)，就可以看到一個全新預設的靜態網頁。  
  
![kykell](https://3.bp.blogspot.com/-KwgGBYcZGLM/V30mD8ULupI/AAAAAAAAKRQ/svf9FTk5VeU8g0Q3RzPLgvmUOnlfdwHlQCLcB/s1600/Screenshot-from-2016-04-26-142241-1024x576.png)  
  
目前先完成了初步在自己電腦端的jekyll安裝設定，至於如何透過git pages來同步把電腦存寫的網頁發佈上網，且待我後續的嘗試。  
  
其它中文參考資料  
[Jekyll x Github x Blog](http://rhadow.github.io/2015/02/18/Jekyll-x-Github-x-Blog-Part1/)  
[Jekyll安裝與範例](https://blog.allenchou.cc/jekyllxfossasia/)

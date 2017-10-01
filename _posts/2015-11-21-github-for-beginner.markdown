---
author: jx tsai
comments: true
date: 2015-11-21 16:32:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2015/11/21/github%e5%88%9d%e5%ad%b8%e8%80%85-%e4%bd%bf%e7%94%a8%e7%ad%86%e8%a8%98/
slug: github%e5%88%9d%e5%ad%b8%e8%80%85-%e4%bd%bf%e7%94%a8%e7%ad%86%e8%a8%98
title: github初學者 使用筆記
wordpress_id: 111
categories:
- coding
- dotlife
- git
- ubuntu
---

![github](https://4.bp.blogspot.com/-jv41aIEmRgw/V3vXpXn8PPI/AAAAAAAAKJc/EOppJwnnmicDrt6EfORaYjXJ4i1vcaLXACLcB/s1600/github.png)  
  
從記錄顯示，我從2014年８月註冊github以來，其實一直很少使用，所以相關的安裝步驟與指令常常是每當需要時才臨時抱佛腳請google大神給予指示。  
  
我想乾脆寫一篇簡單的安裝與指令筆記，留給自己日後參考用，才能日漸累積出對於git指令之熟習能力。也為了寫這篇日記，自己稍認真地重頭試了一次又一次的新手步驟。  
  
1. 安裝git  
叫出終端機，在命令列分別下這二行指令  
sudo apt-get update  
sudo apt-get install git  
（這時應該已經順利在電腦上安裝好了git，不妨在命令列打上：git --version　　可以檢查自己安裝的版本是多少）  
  
2.　設定git  
在命令列下分別打入：  
user.name=Your Name　＃Your Name = github 帳號  
user.email=youremail@domain.com　＃youremail@domain.com = 註冊github所用的eamil  
完成設定後，在命令列打入：　git config --list，　就會出現  
name = Your Name  
email = youremail@domain.com  
顯示到目前為止一切順利  
  
3. SSH Key  
接下來就是要在自己目前使用的電腦上產生一組給github的公鑰,好讓遠端的github 核對加密鑰匙正確後，才會放行資料檔案的修改同步權限，不致造成別人到自己gibhub 資源庫裏亂搞的情況。  
3.1. 在命令列打上：　ssh-keygen -t rsa -b 4096 -C "your_email@example.com"　＃記得把your_email@example.com　改成自己詿冊時所留的電子郵件  
終端機出現：Enter file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]  
（無須輸入，直接按「enter」即可）  
終端機出現：Enter passphrase (empty for no passphrase): [Type a passphrase]  
（要求輸入一組密碼，請依個人喜好習慣輸入密碼後再按「enter」後，命令列會再請我們再輸入一次確認二次輸入的密碼相吻合）  
Enter same passphrase again: [Type passphrase again]  
3.2 將新產生的加密鑰匙加入SSH管理單上  
在命令列打上：ssh-add ~/.ssh/id_rsa  
3.3 用編輯軟體打開 ~/.ssh/id_rsa.pub　這個檔案，複制檔案裏的全部內容。  
3.4 到github 網頁上的個人設定中（personal settings）選擇「SSH Keys」，新增一組「SSH Keys」  
title : 打上自己可以辨認的機器名稱  
key: 貼上前一步驟中　.ssh/id_rsa.pub　檔案內容。  
  
４. 新建repository（檔案庫）  
4.1 在自己的github 網頁上，新增一個repository　（假設該檔案庫名稱為「testdir」）  
4.2 在自己電腦的命令列上，輸入git init　testdir #即為在　git init之後加入自己卻在電腦上初始化一個git repo檔案夾（名稱　為testdir）。則會發現電腦上自動生成了一個testdir資料夾。可以進一步在此檔案夾下的命令列中打上：git status, 查看狀態。  
4.3 繼續此檔案夾下的命令列中打上：git remote add origin git@github.com:yourname/testdir.git # yourname = github帳號  
  
5. 提交檔案到 github 遠端　repository (把自己電腦上的檔案放上github)  
5.1 在欲上傳的檔案夾目錄下,先在命令列打加入欲上傳到github的檔案例如要上傳"text.txt"這個檔案,即輸入  
git add test.txt  
如果要上傳此檔案夾下所有檔案與資料夾,則打入: git add . (注意那個".")  
5.2 在命令列打入: git commit -m "first commit" # -m "XXXXXXX"是指註記的資料,換句話說,不是一定要打first commit ,使用者可以輸入任何要讓自己看得懂的標示資訊.  
5.3 在命令列打入: git push  
  
6. 把遠端 repository　抓回自己的電腦  
命令列下打： git clone git://github.com/schacon/grit.git ＃git:// 之後的網址位置通常就是想抓 repository 的HTTPS 资料，該 repository 不一定得是自己名下的repository，github上公開的repository都可以抓下來。  
  
  
7. 分享自己或複制他人的repository  
目前我都直接先在github 網站上fork他人釋出的repository到自己名下。因為對他人的專案並沒什麼貢獻機會,所以還沒認真學習如何pull request 之類進一步更高階的指令。待日後真的有透過github 和他人協做專案的經驗再來繼續整理吧。

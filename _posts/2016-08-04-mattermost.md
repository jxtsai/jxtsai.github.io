---
author: jx tsai
comments: true
date: 2016-08-04 04:22:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/08/04/mattermost-%e5%ae%89%e8%a3%9d%e8%a8%98%e9%8c%84/
slug: mattermost-%e5%ae%89%e8%a3%9d%e8%a8%98%e9%8c%84
title: mattermost 安裝記錄
wordpress_id: 36
categories:
- opensources
---

![](https://2.bp.blogspot.com/--JaXN6PMVVo/V54ThqgQCNI/AAAAAAAAKp0/dA2n1f76FJkeEBwp4AJwF_n9jzU8Y1tOACLcB/s1600/mattermost.png)  
  
前幾天和幾位「網友」們討論如何強化開源軟件在地化的社群活力，特別是有什麼好工具可以進行專案流程管理與群組溝通,我心裏第一個想到的是：「slack」,不過因為其它人有堅持最好用開源軟的倫理潔癖,所以我就不好意思提出來。後來在推特有看到別人推薦一款替代slack的開源專案協作溝通軟體MatterMost, 這裏[有一篇中文版的介紹](http://technews.tw/2016/03/29/mattermost-usa-student-remote-cooperation/)。因為是開源，就表示可讓任何人試著下載開發中程式碼修正，或是下載穩定版的安裝程式使用。之前有[利用nitrous在遠端工作平台上順利安裝了Kanboard](http://self.jxtsai.info/2016/08/kanboard.html)，想當然爾,如果可以在自己的ubuntu機器上成功安裝MatterMost，那麼在遠端主機上應該也不是難事吧？本文是為在本地端電腦上安裝的過程記錄，遠地端則還在研究如何設定伺服器的環境當中。  
  
由Mattermost官網所提供的安裝文件，在ubuntu環境底有二套安裝方式：第一種方式是分別下載資料庫軟體（PostgreSQL or MySQL)、伺服器軟體（NGINX）、MatterMost伺服器安裝軟體等逐步安裝設定好MatterMost在本地端的運行。第二種方式則其透過docker方式來直接載入Mattermost安裝的映像檔。根據維基百科上的解釋：「Docker是一個開放原始碼軟體專案，讓應用程式布署在軟體容器下的工作可以自動化進行，藉此在Linux作業系統上，提供一個額外的軟體抽象層，以及作業系統層虛擬化的自動管理機制。」嗯，完全看不懂它在說什麼。不過我還是決定先試試看利用docker的安裝法，原因是：它的文件篇幅比第一種方式要簡短許多！！！完全是懶惰地不想看太多文字XDXDXD。  
  
docker 參考資料：[《Docker —— 從入門到實踐­》正體中文版](https://philipzheng.gitbooks.io/docker_practice/content/image/create.html)   
  
一、本地端安裝  
1) install docker on ubuntu   
要利用docker來安裝Mattermost，但前提是電腦得先裝好docker啊，於是先參考了docker官網上如何在ubuntu上安裝的文件：[install docker on ubuntu ](https://docs.docker.com/engine/installation/linux/ubuntulinux/)，這份文件約有一半的篇幅在講安裝docker 的前提環境設定，包括kernel版本檢查, apt source 軟體安裝套件來源列表更新（Advanced Package Tool）等，沒耐心的話，可以直接跳過直奔「Install」部份。（若遇上問題，就再回去看前提環境設定）  
$sudo apt-get update  
$sudo apt-get install docker-engine  
$sudo service docker start ##啟動docker  
$sudo docker run hello-world ##啟動映像檔 hello-world，這是一個檢查安裝docker是否正確的程式，順利的話會回傳成功的訊息。  
  
我照著這些步驟進行，但在最後欲執行hello-world時，卻跑出了：“Cannot connect to the Docker daemon. Is 'docker daemon' running on this host?”的訊息。據說大部份的原因是因為未創建docker群組，所以要再下二道指令  
$sudo groupadd docker #創建docker群組  
$sudo usermod -aG docker ubuntu #紅字部份是放入本機端使用者的id，請以自己登入ID作修改。  
這樣之後還是重新啟動docker，其指令是  
$sudo service docker restart  
這時輸入$sudo docker run hello-world，應該就沒問題了。  
  
2） 安裝好了docker之後，接下來就是透過docker來安裝mattermost  
$git clone https://github.com/mattermost/mattermost-docker.git -b enterprise  ##用git方式抓回下mattermost安裝用的程式檔  
$cd mattermost-docker ##把工作目錄切換到mattermost-docker資料夾  
$docker-compose build ##建立mattermost相關的映像檔安裝, 如果遇上"can't connect to Docker Daemon"的情況，請在前面加上sudo  
$docker-compose up -d     
其中在第三個指令欲執行docker-compose build時，電腦卻回傳以下訊息“docker-compose: command not found”。在網路查了一下問題何在，其在[Stackovweflow上的解答](http://stackoverflow.com/questions/32752360/docker-compose-does-not-install-properly-on-ubuntu-14-04-line-1-errornot-foun)可能是Docker-compose並未適當地安裝好，故可用curl 方式再來安裝（註：curk和 wget 一樣是 linux 中檔案下載時的實用工具）  
  
$sudo su   
$curl -L https://github.com/docker/compose/releases/download/1.4.2/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose  
  
這回妥善安裝好了docker-compose，但執行指令  
$docker-compose buil  
又有另外一個問題跑出來，這回它說： “/usr/local/bin/docker-compose: Permission denied”  
既然是存取權限不足，我自作聰明地以為在指令前面加上「sudo」暫時以root最高管理員身份來執行 docker-compose buil，但也依然無效。原來是得這樣來更改  
資料夾“/usr/local/bin/docker-compose”的使用權限   
$chmod +x /usr/local/bin/docker-compose   
這個指令改好了，基本上 docker-compose buil就應該可以順利執行了。這時候就會看到端終機畫面docker正在自行下載與安裝使用mattermost 相關的軟體套件。整個安裝時間大約十來分鐘吧。  
![](https://4.bp.blogspot.com/-AWoB7w-hGXw/V52T1qWMn5I/AAAAAAAAKoY/qVy5afpINGEIQV8eAx3hL24bIrfeGFGdwCLcB/s1600/docker.png)  
最後一行指令：$docker-compose up -d  ## 則是開始啟動相關的軟體包在後台背景執行。如果到這裏電腦沒回傳什麼奇怪訊息的話，打開瀏覧器，網址列輸入http://localhost/ 就會自動跑出了mattermost，創建帳號的頁面。以後要啟動mattermost 只要將CLI工作目錄切到mattermost-docker目錄底下，再執行這道指令即可運行  
安裝成功！！ ｂ（￣▽￣）ｄ  
![](https://1.bp.blogspot.com/-Rc8oJaqGI8k/V52TXDVoPBI/AAAAAAAAKoU/XFie_pYoP8giR3ulyrddmrU7SwlkajIGQCLcB/s1600/success.png)   
  
因為過程還算順利，心想既然可以在本地端成功裝好，那麼依之前安裝Kanboard的經驗，不妨也同樣來試利用nitrous 工作站下的ubuntu container來操作一遍看看。  
  
二、遠端機器安裝----nitrous  
利用免費帳號，在nitrous開啟一個新工作專案，挑選的雲端開發環境為ubutnu  


![](https://1.bp.blogspot.com/-VRibSh6GvLc/V53fxGCUcqI/AAAAAAAAKpE/4zsJmILvqekPvr4FnZsKaugGg6o5ggNxACPcB/s1600/Screenshot%2Bfrom%2B2016-07-31%2B07%253A58%253A36.png)

  
系統會很快地在幾秒完成建立一個以ubuntu14.04的空容器  
  


![](https://3.bp.blogspot.com/-ac_mxRaIqDs/V59f88Ro4SI/AAAAAAAAKqQ/lSWSvBSjobI2XO-FkfQlesMun9lJJj-TQCPcB/s1600/container.png)

  
接下來依前面一、1) install docker on ubuntu 的相關步驟進行。但是當我試著要啟動docker時，回傳“Cannot connect to the Docker daemon. Is 'docker daemon' running on this host?”訊息，且試過前述新增使用者，或其它網路上找到的方法都無法解決。按nitrous.io上面對於用戶不同付費方案的說明，表示即使免費版用戶仍有提供docker功能，但到底要如何查出設定過程中的問題，我還在努力當中。  


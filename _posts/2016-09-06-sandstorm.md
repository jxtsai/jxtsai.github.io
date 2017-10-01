---
author: jx tsai
comments: true
date: 2016-09-06 06:58:00+00:00
title: sandstorm 使用
category:
- dotlife
- opensources
---

  
因為之前試著安裝Rocket.chat，想找找除了Nitrous.io之外，是否還有其它提供免費帳號試用的PaaS（platform as a service），故在其建置佈署文件中找到了這家sandstorm.io。一開始只是在其示範型的網頁（https://oasis.sandstorm.io）註冊一個帳號試用。使用者在完成免費版註冊後可以取得200MB的儲存空間（訂閱其電子報可以再加1G空間），以及5個網頁應用程式軟體的安裝使用（其單位叫作"Grain"剛好叫作五穀？)。  
  
oasis.sandstorm.io會員登入後所看到的畫面：  
![](https://4.bp.blogspot.com/-RIkjOjWMdzc/V81etWemAEI/AAAAAAAAK1E/cn34YN51QYgiiPYoxfYw13kfI2B8XUCcgCLcB/s1600/app%2Bmarket.png)  
在它的App Market 已經放上了不少開源的網頁應用程式，也就是透過瀏覧器可以執行：程式開發環境，如Ｉpython Notebook；辦公室常用軟體，如試算表EtherCalc，待辦事項清單simple todos,投影片製作hacker slides;或是團隊協作使用的專案管理工具WeKan, Rocket.chat等等各式的軟體。用戶只要一點欲安裝使用的軟體，它就會在幾秒鐘之內建立好出現在自己的Grains底下，而這些網頁應用軟體也可以透過分享權限方式讓其它人可讀取、編修、溝通。  
  
這兩天想仔細了解sandstorm.io的價格方案，才明白原來sandstorm本身就是一個開源的個人雲平台軟體，任何使用者免費下載將它安裝在自己的電腦之後，就可以透過瀏覧器來安裝執行辦公室工作軟體、專案管理軟體。當然前提是，sandstorm得運行在連上網路的linux系統中，且最好有１GB以上的記憶體空間。它的安裝說明頁表示，最好在使用的雲服務上建置一部運行ubuntu 14.04 64位元的虛擬機器，而我目前使用的二台筆電都是ubuntu 14.04 64位元作業環境，根本不必另開模擬器，故決定來試試安裝在筆電上面。  
  
據其安裝文件共提供了７種安裝方法選項介紹,因偷懶我採用第一種，也是最簡單的HTTPS-verified install（但可能相對在安全認證上較不嚴謹），直接在terminal文字指令列上打入：  
$curl https://install.sandstorm.io | bash  
就會自動開始進入安裝程序，並詢問是要進行: 1 一般安裝 2 本地開發模式安裝　##因為我沒有租用任何雲機器空間，當然是選擇２在本地端機器安裝模式  
![](https://4.bp.blogspot.com/-hVfiipIOZzA/V80Mu1IcV4I/AAAAAAAAK0o/NVPKgJwH7GkxCku-IGexgzN4v7Ug6FSDQCLcB/s1600/mode.png)  
  
不出十幾廿秒下載安裝完成，它會顯示一組本地網址資訊，只要點擊它自動開啟網頁就會看到下面的本地端開發者登入畫面：  
dev account  
![](https://2.bp.blogspot.com/-lWoI63xK7Po/V80MkQoTQOI/AAAAAAAAK0k/zpYri4MfRDAogDUfcx77UbzZFOzG4dkgQCLcB/s1600/dev%2Bacc.png)  
![](https://1.bp.blogspot.com/-KRmzvWc3FsM/V80N0ePe8BI/AAAAAAAAK0w/2WGo61FO5LcfB89JcAoeMHtbihoLzZJ2wCLcB/s1600/welcome.png)  
  
當然在本地端，連上網的用戶也可以在其web app market安裝https://oasis.sandstorm.io上所有列出的應用軟體,同樣是一鍵就可以輕鬆完成安裝，不過這個軟體只能在本地端電腦的瀏覧器上執行，並沒有發佈到網路上。例如我挑選了透過sandstorm.io安裝wordpress，它就會連網自動安裝好，在Grain列表出現wp ,以及下方熟悉的ＷＰ後台管理介面。  
![](https://2.bp.blogspot.com/-Mp8tzr-LQSQ/V81pvI8wHJI/AAAAAAAAK1g/BM4WdnLy_8EVhTCoKyLw8X-irEzIsnSSgCLcB/s1600/wordpress.png)  
  
![](https://1.bp.blogspot.com/-ejzUCPh42Ys/V84eMmdfQMI/AAAAAAAAK1w/4g8BIMkTEYgS2tmjp9SCSmR_mhBDzz88wCEw/s1600/downloading.png)   
通常某些APP會再提供指紋或密鑰比對認證，以確認該軟體未遭惡意修改破壞  
![](https://1.bp.blogspot.com/-i3Q6bjVqui4/V84er7GL6mI/AAAAAAAAK10/ofnklHWdw4UEIQIAdg6T5DunEj3EGOXnACLcB/s1600/keys.png)  
  
sandstorm.io在本機安裝可以作什麼用？  
既然不是在雲端機器的佈署，也不是應用軟體開發者打算來寫相關web app package 發佈供應在sandstorm.io市集使用，那麼在本地機器上安裝sandstorm.io有什麼意義呢？嗯。。。。，大概就是能讓自己想像一下：在瀏覧器環境下安裝使用etherPad，WeKan，RocketChat等玩意的感覺是如何吧。  
  
sandstorm.io　其它中文介紹資料[  
http://www.freebuf.com/sectool/43879.html](http://www.freebuf.com/sectool/43879.html)

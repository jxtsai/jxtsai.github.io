---
author: jx tsai
comments: true
date: 2016-01-07 08:40:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/01/07/%e5%8a%a0%e8%a3%9dssl%e7%b6%b2%e8%b7%af%e5%ae%89%e5%85%a8%e6%86%91%e8%ad%89%ef%bc%88lets-encrypt%ef%bc%89/
slug: '%e5%8a%a0%e8%a3%9dssl%e7%b6%b2%e8%b7%af%e5%ae%89%e5%85%a8%e6%86%91%e8%ad%89%ef%bc%88lets-encrypt%ef%bc%89'
title: 加裝SSL網路安全憑證（Let's Encrypt）
wordpress_id: 99
categories:
- dotlife
- encrypt
- privacy
---

過年前看到免費資源網路 社群上有一篇「[SSL For Free 免費 SSL 憑證申請，使用 Let’s Encrypt 最簡單方法教學！](https://free.com.tw/ssl-for-free/)」文章，想說不妨在自己的網站上試試。  
  
雖然我租用的ipage 網頁空間其後台虛擬主機控制軟體是C penal, 但由於服務提供商尚未導入「[ Let’s Encrypt](https://letsencrypt.org/)」的 SSL 免費憑證功能，只好先透過第二種方法，也就是利用SSL For Free 線上工具，來連接 Let’s Encrypt 的憑證簽發功能，其優點是安裝直覺容易只消兩三個步驟即可，但缺點是要（每90天）定期地更新憑證。  
  
![let's encrypt](https://letsencrypt.org/images/howitworks_certificate.png)  
  
由於我的部落格是使用WORDPRESS架設，故進一步再參考同一網站介紹方法：[在 WordPress 設定 HTTPS，強制使用 SSL 安全加密協定教學](https://free.com.tw/moving-to-https-on-wordpress/)，(主要是更新資料庫裏面的舊連結)讓全站的文章與圖片都順利完成了「可使用SSL」的設定（也就是本站內的站內連結都自動成了https://,　多了一點s）。  
  
至於安裝SSL的理由和好處是什麼呢？  
  
其一是去年，google 宣佈將保密安全要素也列入其決定網頁搜尋排名決定的考量因素，因此引發一陣企業網站加購SSL服務的風潮（？），當然這倒不是自己在自家網站上試著安裝SSL的主要動機。  
  
其二主要仍是自己好奇的練習，衝著「[Let's Encrypt](https://letsencrypt.org/)」打著開源免費的服務，不妨來試試嚐鮮。特別是去年學習了一點[GNU GPG的皮毛](http://self.jxtsai.info/2015/09/gpg.html)，除了這種點名式點對點的內容金鑰加密方式外，或許可以讓我稍再了解一點所謂[網路安全傳輸的運作原理](https://letsencrypt.org/howitworks/technology/)。（其實現在仍是懵懵懂懂啊）  
![let's encrypt](https://letsencrypt.org/images/howitworks_challenge.png)  
![let's encrypt](https://letsencrypt.org/images/howitworks_authorization.png)  
  
最後是網路通訊加密技術 ，顯然將在後Snowden時代與一直進行式的「反恐行動」中，將被合法暴力機構宣稱其已變質成打擊激進宗教邊緣狂熱武力組織的反挫工具，以降低人民在網路通訊上原來抱有的隱私合理期待，這樣「監聽合理存在」將剝奪人民享有祕密通訊之言論自由。或許這樣的擔憂是太早了一點，但在國家／企業侵蝕奪走我對於隱私合理期待的標準底線不斷撤退投降之前，不妨先玩玩一點小工具，看看能做一點什麼無關緊要的反抗吧。進一步參考：[SR on FOE 2-15聯合國人權理事會報告-網路加密匿名與人權框架](http://self.jxtsai.info/2015/05/sr-on-foe.html)。

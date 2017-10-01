---
author: jx tsai
comments: true
date: 2015-09-11 10:47:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2015/09/11/gpg%e5%8a%a0%e5%af%86%e9%87%91%e9%91%b0/
slug: gpg%e5%8a%a0%e5%af%86%e9%87%91%e9%91%b0
title: GPG加密金鑰
wordpress_id: 122
categories:
- encrypt
- privacy
- tactical technology collective
---

之前曾經試著依樣畫葫蘆的想來試試安裝使用GPG這類的網路加密軟體，目的倒不是為了什麼通訊保密上的安全，而是讓自己看起更geek一點XD。不過當時（約半年前）按圖指示操作了半天還是有點似懂非懂，而且自己連平日互通郵件的往來者都沒有，哪還需要搞什麼加密安全通訊Orz。  
  
不過近來看了 [Tactical Technology Collective](https://tacticaltech.org/projects/decrypting-encryption)（本人最愛的NGO之一）所製作推廣GPG的動畫，且這半年，自覺在操作Command-line interface比較知道是在幹嘛，故決心這次來好好來搞清楚如何使用GPG。   
  
  
  
因為我目前習於使用linux系統下ubuntu家族的作業環境，設定過程主要參考了這篇文章：[GPG入門教程](http://www.ruanyifeng.com/blog/2013/07/gpg.html)，作者一步一步仔細耐心的中譯說明，讓我算是比較清楚地了解如何製作生成自己的一組GPG金鑰。（另外一篇可參考的是洪阿貴老師的文章：[使用GnuPG建立PGP金鑰， 讓別人能夠私密寄信給你 ](http://newtoypia.blogspot.tw/2013/12/gnupg-pgp.html)，但因為阿貴老師的文章太幽默白話，魯鈍如我要用力看好幾遍才能看懂XDXD）  
  
我GPG的公鑰資料存在這裏：[me(at)jxtsai.info](http://www.jxtsai.info/blog/files/jxtsai.txt)  
  
既然安裝好了GPG，也成功地申請了一組公私鑰，那麼接下來要怎麼使用呢？ 我的理解是這樣：如果有人（姑且稱之為某甲）要寄給我一個極重要的資料，又不能隨意透過一般的電子郵件或傳真送出，若某甲想透過GPG加密，則依下列步驟進行:  
  
1）在自己在的電腦上，按照前述的步驟安裝好GPG程式（windows 或蘋果 OS 系統安裝GPG請參考這裏:[使用Gpg4Win進行加密](http://blog.timshan.idv.tw/2013/09/howto-gpg4win.html) 和那裏:[Install the GPGTools GPG Suite for OS X](http://notes.jerzygangi.com/the-best-pgp-tutorial-for-mac-os-x-ever/)）  
  
2）某甲成功安裝好GPG並產生自己一組公私密鑰之後，把我的公鑰加入到某甲自己的GPG認可名單中。（linux下指令： $gpg --import jxtsai.txt）  
  
3）透過指令操作，把要給我的機密資料予以加密。這時候產生的加密文件，就一定只有配對我這把公鑰的另一組私鑰，才能開啟。  
（指令：$gpg encrypt secret.txt ）  
  
下了指令後，電腦會詢問此檔案的接收對像是誰？只要輸入接收者的ID（或email）, 便會在同一個資料夾下，自動生成一個 secret.txt.gpg 的加密檔案。註：無法使用MS Office儲存原始資料檔案格式（doc, docx），一般就只是把機密內容貼成一個txt或asc的純文件格式即可。  
  
4）把加密的資料檔案（secret.txt.gpg），按一般傳輸方式，寄到我的信箱本人。我收到檔案後，透過自己的私鑰就能開啟此加密檔案。其它人如果收到或攔截到此加密檔案，因為沒這把私鑰，所以幾乎是不可能解開。（指令 >gpg --decrypt secret.txt.gpg, 然後就會再進一步詢問你的私鑰密碼，如果輸入正確就會解開secret.txt 內容）  
  
後來聽了Coursera 課程「Internet History and Security」,才知道原來這種公私加密金鑰與配對檢驗的安全保護作法，其實早已在許多網路程式裏日常地被實踐著，但一般使用者卻無所知覺，也多不深究其原理。例如以往會被敎育，如果要在線上使用信用卡就要確認該網站是否有提供加密憑證（SSL），簡單來說就是在我不知道的過程中，已經和欲在其上交易的網站進行了一場密鑰交换的過程，交易網站透過我電腦所提供的公鑰，加密了我交易的財務信用卡資料，也只有我授權同意交易的網站服務，才能用他們的私鑰來解密其信用卡資訊以確保交易的完成。我之前不知道原來背後就是靠著這樣的方法，來維護我們在線上購物付款的資料加密安全啊。  
  
同理反推，如果網路上交換的資訊未經加密動作，那麼任何的往來郵件，瀏覽記錄，聊天內容，就**如同用明信片一樣沒有密封**，有心人士攔截後就可以輕易察看其內容。明信片這個準確的比喻，或許就是大家在評估通訊內容私密與否，要不要多一道手續加強防衛的判斷囉。  
  
簡介加密與密鑰的原理小短片  


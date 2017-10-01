---
author: jx tsai
comments: true
date: 2016-09-22 07:42:00+00:00
title: python smtplib 練習--寄電子郵件
category:
- python
---

[![](https://2.bp.blogspot.com/-K3BgEeV8XDQ/V-OJLqep6NI/AAAAAAAALBk/VdNVQ_VCPzwP515Dcf5Xk4ZW3fdiwhaKQCLcB/s1600/send-emails-gmail-python.jpg)](http://stackabuse.com/how-to-send-emails-with-gmail-using-python/)

image from stackabuse

  
原文出處　[MotherBoad Hack This Serial ](http://motherboard.vice.com/read/how-to-send-an-email-from-a-python-script)   
  
0) 了解電子郵件通訊協議基礎知識　email protocols  
POP (Post Office Protocol) 早期電子郵件傳送協議，通常用於電子郵件軟體，透過ＰＯＰ協議連接遠端郵件伺服器，並取得其上郵件帳戶資訊（如收電郵）  
IMAP (Internet Message Access Protocol) 目前互聯網使用的電子郵件標準協議。近十年來成為主流的webmail，即是採用IMAP協議，但其透過多一層網頁瀏覧器的HTTP協議好透過網頁收取電郵。　  
Simple Mail Transfer Protocol (SMTP)，傳送寄出電子郵件則會用到的是　SMTP協議。有興趣深掘可以看看１９８２年互聯網工程任務組IETF還沒成立之前,Internet 前身始祖ARPANET時代的RFC821號文件  
  
1)　引入Python SMTP module模組  
Smtplib 是python已一起附好的函式庫模組，故不必另行下載安裝，但在寫程式碼時，仍然要透過import引入該函式庫模組  
在CLI環境下進入python interpreter(python 直譯器) , 引入該模組函式庫import smtplib, 若輸入 help(smtplib) 透過help函式來叫出smtplib的指引文件  
[![](https://2.bp.blogspot.com/-tcWiRsTeGbQ/V-KAs7L0kJI/AAAAAAAAK_Y/PDt8Ww8FilME_DMhIesYP_27ifMcucehQCLcB/s1600/smtpcli.png)](https://2.bp.blogspot.com/-tcWiRsTeGbQ/V-KAs7L0kJI/AAAAAAAAK_Y/PDt8Ww8FilME_DMhIesYP_27ifMcucehQCLcB/s1600/smtpcli.png)  
![](https://2.bp.blogspot.com/-M6YZ1UHmsNM/V-J9eP3aVxI/AAAAAAAAK_I/JH9GgHOCYastT6k2qFIFGxi0zGCKNdgBACLcB/s1600/smtplib.png)  
  
當然如果不習慣從終端器軟體介面讀取文件，可以直到到python官網上查閱[smtplib 的用法](https://www.blogger.com/docs.python.org/library/smtplib)  
  
smtpObj = smtplib.SMTP('smtp.gmail.com', 587)   
#宣告smtpObj 此變數，指定其為一個smtplib模組的SMPT類別class實體instance，換言之，smtpObj這個instance 也會繼承了SMPT類別class當中所包含的功能函式method，並可透過.方式來叫喚出某個功能。  
想好好弄清楚　python modules/ class /instance 觀念，建議多翻幾次  
Ｌearning Python the Hard Way :[Modules, Classes, and Objects](https://learnpythonthehardway.org/book/ex40.html); [Is-A, Has-A, Objects, and Classes](https://learnpythonthehardway.org/book/ex42.html)這二章的說明。  
  
smtpObj.starttls()  
#這是instance smtpObj 必須在安全傳輸的圖層協議Transport Layer Security　protocol來進行連結傳輸,故叫喚starttls這個函式。我曾試著把這行取消（其風險就是在執行該程式碼時，包含程式碼上電郵密碼明文，在會無加密狀況下在網路中旅行），結果按gmail目前傳送協議，傳送回來了失敗的訊息。  


![](https://1.bp.blogspot.com/-ePtMKrWZU6Q/V-Ne_KXYJGI/AAAAAAAALAw/3K0QMQJuAWUsiCI0OLnsWslQcnN8BBDfACLcB/s1600/tsl.png)

  
我先按照網路上查到的[方式先作是否連通測試](http://stackabuse.com/how-to-send-emails-with-gmail-using-python/)，一直傳回出錯的訊息。最可能的原因是來自gmail 對於可疑app要求登入許可的請求拒絕。因此要到gmail帳戶下，先暫時選取[安全性較低的應用程式許可設定](https://www.google.com/settings/security/lesssecureapps)。  
  
當確認smtpObj可以連接smtp遠端郵件伺服器並成功登入後，接下來要做的就是好好地寫一封信件，並將其寄出。  
第一種寫法：  
  
成功地收到郵件了，Ｏ耶～  


![](https://4.bp.blogspot.com/-Gn7JIlxElP4/V-NTrbDLTFI/AAAAAAAAK_8/7B2wSi00pWMVYzPNcEyI3RScAS8Kelm-ACLcB/s1600/successful2.png)

第二種寫法  
  
也同樣成功地收到郵件  


![](https://1.bp.blogspot.com/-qlFb4rXogXY/V-NVTiqGynI/AAAAAAAALAI/wwQvdIg00T0n_9aFL89iOyMlFoictN1YACLcB/s1600/success.png)

其中要注意sendmail這個函式帶了五個參數，前三個為必要，sendmail(from_addr, to_addrs, msg, mail_options=[], rcpt_options=[])  
第一個參數from_addr是為字串型態的數值，而to_addrs則為list的資料型態, msg 則亦為字串型態。我不太了解，為何第二種寫法，為何可以讓電郵主旨成功地出現在郵件的主旨欄位。而第一種寫法則郵件主旨內文都整個擠到電郵內容當中。  
  
除了gmail外，我還試了其它的「一般」郵件伺服器，例如我在ipage.com 租用的虛擬主機有包括郵件服務，用它來試寄電郵，結果一直沒收到信，原來是遭到收件方google的郵件伺服器回應判讀這封信件為垃圾詐騙因此無法傳送遭到了退回。  


![](https://4.bp.blogspot.com/-d9Bbdowz21g/V-OFc-XhnJI/AAAAAAAALBM/Q8vD2kVd_BkCjpD-GrO5GdyWktgEsqJYQCLcB/s1600/spam.png)

  


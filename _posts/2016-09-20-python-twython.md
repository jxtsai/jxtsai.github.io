---
author: jx tsai
comments: true
date: 2016-09-20 08:29:00+00:00
title: python Twython 練習
category:
- python
---

小人常立志要自學電腦程式，但鄙人程度不但沒什麼進展進步，而且過一陣子沒碰某個程式語言後，就很快地忘光它的基本語法和重要內建功能。自己又不太能專心一意地試作小型專案，故利用「仿作」方式，以查讀相關文件重溫程式規則語法以及函數功能，來進行習作練習。本篇原文出處：[https://motherboard.vice.com/read/hack-this-automate-your-twitter-in-10-lines](https://motherboard.vice.com/read/hack-this-automate-your-twitter-in-10-lines)，　其透過python程式語言及其強大的函式庫模組,以在文字指令界面下操作玩簡單的twitter各種功能。  
  
1. 在twitter　deve上申請一個專用ＡＰＩ  
要先取得ＡＰＩ的接口授權，才能夠抓取相關原始數據資料。  
  
2. 假設電腦上已有python ，請再下載安裝 tweepy / Twython這兩個強化python功能的函式庫模組   
有多種方式可安裝python 模組，例如利用pip(Python Package Index),即python的套件管理程式。  
$pip install twython  
$pip install tweepy  
或是先把二者的原始碼clone下來後，利用python setup.py install指令安裝  
  
Twython 這個套件本身為用來取得twitter資料數據，從[其文件說明介紹，](http://twython.readthedocs.io/)它可以用來搜尋（用戶資料、lists、時間軸等資訊）,或是上傳更新用戶的照片圖片。  
例如利用update_status這個功能，可以透過python 執行該程式碼來更新自己推特狀態  


<blockquote>twitter.update_status(status=‘See how easy using Twython is!輸入更新的訊息!')  </blockquote>

##括弧內單引號內的文字即是想要輸入的狀態更新訊息，目前測試亦支援中文輸入  
![](https://1.bp.blogspot.com/-HhbPv5eo_Y8/V-CjMKgh3DI/AAAAAAAAK6s/t97guz8_ZNAxlztvwipRb35CNui5jY1OwCLcB/s1600/twyphone.png)![](https://3.bp.blogspot.com/-ZbvtAu7-Jss/V-CjSRGwa1I/AAAAAAAAK6w/vDgdoNcv8o4QebXbsKULlh3pTwIFMasrQCLcB/s1600/update-zh.png)  
  
當然別忘了，要進行這個小試驗之前，要在這支python程式碼上引入Twython函式庫,並且將Twython method所需的參數資料依照自己的twitter Dev API值設定填好。在Twython使用文件的進階版介紹中，還說明了若要插入影片或照片作更新twitter的方法：[Advanced Usage](https://twython.readthedocs.io/en/latest/usage/advanced_usage.html)　  
  
3. Twython進階使用  
經過前面簡單測試過了twython的入門使用小功能後，現在要進一步摸索Ｔwython進階使用。  


<blockquote>timeline = twitter.get_home_timeline(screenname='a5288',count=50)　</blockquote>

##screenname 是twitter帳號，用這支 get_home_timeline　method會抓回一串很長json格式的資料。其內容之複雜，實在讓我不知道怎麼整理乾淨。(如果要看到timeline的內容，別忘了要利用print功能把資料內容印出到螢幕上)  
##原文雖然可以在此處參數中的screenname='XXXX'輸入欲抓取任何一位用戶時間軸上的推文，但我試過似乎只能抓回自己時間軸上的推文，否則那就太可怕了。故此處若省略screenname=''這組參數，其效果仍然一樣。而count則是欲取抓取的時間軸上的推文數量。以我個人在某個時間透過這個方法，抓回一則自己推特時間軸上的推文,其回傳的資料內容如下：  
在瀏覧器上所看到的這則推文資訊內容：  
![](https://2.bp.blogspot.com/-xb4cJuLEHhE/V-DX4xM1u6I/AAAAAAAAK7M/Pxl6iDrWTxg0J-ezgyF8edzLDh4HgaXxACLcB/s1600/tweet_gijn.png)  
抓回內容為python dinctionary 資料類型，Twython 已將其轉換為Json格式  
  
光一則推文的元數據/鍵值key/ tag 實在令我大開眼界，不過在此尚不必用到這麼雜亂的資料，故回到作業程式碼檔案，如果在再入底下二行，則會回傳打印出想要顯示在螢幕上的資訊，如推文內容以及發文者  


<blockquote>for tweet in timeline:  
print (tweet['text'] + "by " + tweet['user']['name'])</blockquote>

  
執行完此支程式後，即在ＣＬＩ界面回傳我的推特時間軸上的前十個推文與發文用戶  
![](https://4.bp.blogspot.com/-Sbw80zHwR3w/V-DdPM38H7I/AAAAAAAAK7k/u4awJxl0YF4seJQVgb9j98QLwQON-mjRwCLcB/s1600/return-tweets.png)  
  
下面這段程式主要目的是除了透過執行python程式抓取自己時間軸上的某一則答符合查詢條件query的推文外，並且把這則推文列成自己喜愛收藏的推文（ＬＩＫＥＳ）。  


<blockquote>twitter Twython(APP_KEY,APP_SECRET,OAUTH_TOKEN,OAUTH_SECRET)  
def fave(query,t,count=50):  
tweets = t.search(q=query,count=count)  
for tweet in tweets['statuses']:  
result = t.create_favorite(id=tweet['id'])  
print("favorited " + result['text'])  
query = 'Censorship Machine'  
fave(query,twitter)</blockquote>

##寫一個名之為fave的函式(function)，再加上利用Twython內建寫好的函式，如create_favorite，即可來操作新增符合查詢條件的推文成為自己喜愛的收藏。fave的第三個參數count符合查詢字的推文最多數量。原文中倒數第三行print("favorited " + result['text'].encode('utf-8'))，我若加了encode('utf-8')反而無法正常顯示字碼，故將其刪除  
  
4. TwythonStreamer　[使用者文件](http://twython.readthedocs.io/en/latest/usage/streaming_api.html?highlight=TwythonStreamer)  
這裏我們進一步利用Twython函式庫當中的TwythonStreamer 功能,當然別忘了在程式一開始，就要把這支TwythonStreame呼叫進入，以便接下來直接使用它人寫上的功能應用。  


<blockquote>class MyStreamer(TwythonStreamer):  
def on_success(self, data):  
if 'text' in data:  
print (data['text'])  
def on_error(self, status_code, data):  
print (status_code)  
  
stream = MyStreamer(APP_KEY, APP_SECRET,  
OAUTH_TOKEN, OAUTH_SECRET)  
stream.statuses.filter(track='HRC33')</blockquote>

從原始碼來看，這裏利用了TwythonStreame功能來建置一個叫作MyStreamer的類別class,這個類別中設定了二項功能，一個是on_success成功狀態下打印出資料內文訊息，一個是出錯on_error則打印出狀態碼。最後再新增變數stream，其即為MyStreamer類別，故其會繼承MyStreamer所具備的功能。這裏的track是指查詢關鍵字，這個程式碼執行時，它會自動抓取twitter時間流（似乎並不限於原帳戶時間流）中符合查詢關鍵字的推文。  
![](https://1.bp.blogspot.com/-9Oi5Mm6mFsM/V-DqSLHWiiI/AAAAAAAAK8A/pJbNYyNAzQkol45YWguAGzLTHiAGhDGgACLcB/s1600/hrc33.png)

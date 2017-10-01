---
author: jx tsai
comments: true
date: 2015-05-20 11:02:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2015/05/20/impress-js-%e7%b0%a1%e5%a0%b1%e8%bb%9f%e9%ab%94/
slug: impress-js-%e7%b0%a1%e5%a0%b1%e8%bb%9f%e9%ab%94
title: impress.js 簡報軟體
wordpress_id: 142
categories:
- javascript
- multimedia
- ubuntu
---

之前有簡單提過自己學著用向量圖片編輯的開源軟體 [inkscape 外掛sozi](http://self.jxtsai.info/2015/05/ubuntu-sozi.html)，來做出如prezi 一樣酷烗的簡報檔案。自己當年也曾經一度愛用prezi來做簡報檔，當然是比起微軟office suite 當中又呆又醜的PPT，可以扭來動去的prezi自然是給實質內容不怎麼樣的演講簡報大大地加分XD。不過prezi 還有一些小問題，例如對中文字型的支援不足，而且它貌似完成品為flash檔案格式，實不利於內容搜尋（如同一家公司ADOBE 開發的PDF格式文件，雖然成了網路上文件檔案的主流，但因其不利搜尋，也是遭提倡網路高度開放者之垢病）   
  
![](http://www.webresourcesdepot.com/wp-content/uploads/impress_js.jpg)  
  
這兩天看到有人推薦用javascript　網頁互動與前人開發之JS函數資料庫寫成的[impress.js](https://github.com/bartaz/impress.js)，它充分利用結合HTML與CSS，把網頁HTML變成了一份活潑的簡報。要使用impress.js 製作簡報，操作者或許不必了解太深的javascript 語言，還是得要對於HTML CSS有一點基本正確的知識能力。幸好有人已致力於開發一些所見即所得的編輯軟體工具，What You See Is What You Get，WYSIWYG），例如[Ｓtrut](http://strut.io/editor/),或許可讓impress.js之推廣應用能更為普及。  
  
如果不是採上述視覺化的編輯器，利用impress.js 所作的簡報檔，當然是得回歸原始的HTML文字編輯下。在新建（或複制）一個html檔案下，除了建立好網頁與js檔案的連結外，文件中若要新增一個投影格，即是寫出以下html程式碼：  
`  


  
My first slide　（PTT 一張一格的投影片樣式，其內容可自行更新，**當然還是得注意html語法**）  


  
  


  
My first slide　（簡報則成了一張大畫布，每面要呈現的內容可在其上自行更新）  


  
`  
  
data-x = the x co-ordinate of the slide　投影片內容水平移動之設定  
data-y = the y co-ordinate of the slide　投影片內容垂直移動之設定  
data-z = the z co-ordinate of the slide 投影片內容前後移動之設定  
data-scale = scales your slide by a factor of this value. 投影片內容大小之設定  
data-rotate = rotates your slide by the specified number of degrees　投影片內容旋轉角度設定  
data-rotate-x = For 3D slides.  This is the number of degrees it should be rotated about the x-axis.  (Tilt forward/lean back)　投影片內容立體水平移動之設定  
data-rotate-y = For 3D slides. This is the number of degrees it should be rotated about the y-axis (swing in from the left/right)　投影片內容立體垂直移動之設定  
data-rotate-z = For 3D slides. This is the number of degrees it should be rotated about the z-axis　投影片內容立體前後移動之設定  
  
[How To Use Impress.Js]()  
  
我自己對於PTT（impress of Libre Office,）, Prezi, Sozi, impress.js 這幾套簡報軟體使用下來，其實impress.js 的操作上，不比sozi這種已建構視覺化的編輯器優勢，但是如果作者有心想多加練習自己在hmtl, css ,js 語法功力，花點時間上手學會熟悉impress.js　指令，應對加強CSS, DOM, JS library之認識有所助益吧。  
  
延伸閱讀：　[HTML 簡報，html5slides, deck.js, impress.js 使用心得](http://www.icoding.co/2012/07/html-html5slides-deckjs-impressjs-html)

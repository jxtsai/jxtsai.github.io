---
author: jx tsai
comments: true
date: 2016-09-21 06:43:00+00:00
title: python PIL練習
category:
- python
---

繼續透過Motherboard HackThis系列文章的「仿作」方式，一邊溫習簡單的python語法規則，一邊查讀相關文件重溫程式規則語法以及函式功能。本篇原文出處[Hack This: Edit an Image with Python](http://motherboard.vice.com/read/hack-this-edit-an-image-with-python)，　  
利用python及其函式庫來進行圖片的編輯修改。（噁，雖然用圖片介面ＧＬＩ的圖像編輯軟體如Adobe 旗艦商業軟體PS，或是對一般用戶基本需求功能不輸ＰＳ的開源自由軟膿ＧＩＭＰ，其使用便利已遠遠超過花時間寫python程式碼來做圖片編輯，但目的當然不是要編修照片，而是透過了解python以及相關函式庫,來練習程式學習）  
  
1. [Pillow](http://)入門基礎模組Ｉmage  
同樣先透過pip(Python Package Index),即python的套件管理程式，來安裝　Pillow  
$pip install Pillow  
Pillow　是ＰＩＬ的進化版，而PIL則是Python Imaging Library之意，從它的[使用文件資料](http://pillow.readthedocs.io/en/3.3.x/)中，可以看到其具有十多種圖片編輯之模組，例如其[Image　module](http://pillow.readthedocs.io/en/3.3.x/reference/Image.html)　底下就有幾十種功能，有空不妨照著它的文件來試試這些功能如何能使用。例如在motherboard 原文中介紹的thumbnail,即可以照片改成size指定的尺寸大小。（我另外試了rezise功能，但它是照片的檔案變小，但像素大小卻未改變）  


<blockquote>from PIL import Image, ImageFilter  
img = Image.open('jpl_pioneer_galaxy_full.jpg')　  
size = (640,640)  
img.thumbnail(size)  
img.save('main_jpl_pioneer_galaxy_full_small.jpg') </blockquote>

而另一個Image.filter功能，則是在括弧（）內放入欲應用的ImageFilter模組的method,如　BLUR，　CONTOUR，　DETAIL，　EDGE_ENHAN, EDGE_ENHANCE_MORE, EMBOSS, FIND_EDGES, SMOOTH, SMOOTH_MORE, SHARPEN等基本濾鏡功能  
  
如下圖，是利用ImageFilter.BLUR作出的模糊化效果  


![](https://2.bp.blogspot.com/-kIMI81ujZM0/V-IB9gzt8tI/AAAAAAAAK8w/ZVw9swyQdpwzYsqBAQsHN4iAmoUnl6C1ACLcB/s1600/blurred.jpg)

from PIL import Image, ImageFilter  
img = Image.open('jpl_pioneer_galaxy_full.jpg')　  
img = img.filter(ImageFilter.BLUR)  
img.save("blurred.jpg", "JPEG")  
  
另外ImageFilter底下還有一些類別class，　例如用這個[高斯模糊](https://zh.wikipedia.org/wiki/%E9%AB%98%E6%96%AF%E6%A8%A1%E7%B3%8A)濾器　img = ImageFilter.GaussianBlur(radius=5)  
![](https://4.bp.blogspot.com/-cmvq-2Kux_Q/V-IGeSVoJYI/AAAAAAAAK88/Cm_9STejUN02mzUCfBHVSXfEUw1ONrohQCLcB/s1600/18602753328_921acecf53_o.jpg)  
![](https://3.bp.blogspot.com/-2vC05z_eTnQ/V-IGmydcW3I/AAAAAAAAK9A/cfV6mmDKblE5CCrL3PWpQFmCEm87psIbwCLcB/s1600/pic.jpg)   
第一張為原始照片，第二張則是修改過的，據說它的作妦在減少圖片雜訊及降低細節層次，其視覺效果如同經由一個半透明的濾鏡來觀察圖片，當然其參數radius可以自行調整所欲的數值。  
  
2. ImageChops 模組  
根據其使用文件的說明，這個模組是透過圖片運算操作來進行圖片的修改編輯。例如ImageChops.add()  
可以把二張照片合成為一張  
from PIL import Image, ImageChops  
img1 = Image.open("pic1.jpg")  
img2 = Image.open("pic.jpg")  
img3 = ImageChops.add(img1, img2, 1, 0) ##括弧中的後兩個參數分別代表scale 與offset 後者應是指二張照片相應之對比，而scale則是其對比程度  
img3.save("add1.jpg")　  
  
下二張照片，第一張scale＝１　offset = 0, 第二張　scale＝１　offset = ２  
![](https://3.bp.blogspot.com/-Lsxl2L3zAaI/V-ILnzJd-JI/AAAAAAAAK9Y/ac3sO6Ys5hMwgTMgQk9TbKO-VKKMR0h5ACLcB/s1600/add1.jpg)　  
[![](https://2.bp.blogspot.com/-0H-s1v_AjaM/V-ILvOuQ61I/AAAAAAAAK9c/tm6cnombDTQK6JLOoyK8PXxrghQgAi-6wCLcB/s1600/add2.jpg)](https://2.bp.blogspot.com/-0H-s1v_AjaM/V-ILvOuQ61I/AAAAAAAAK9c/tm6cnombDTQK6JLOoyK8PXxrghQgAi-6wCLcB/s1600/add2.jpg)  
  
本習作使用的二張原始照片  
![](https://1.bp.blogspot.com/-NGwE9X58kqc/V-InUUK8hkI/AAAAAAAAK-Q/P3p_4SKUEvsOhYWhSjEv2Yw25TlJq6DQQCLcB/s1600/pic.jpg)  
![](https://1.bp.blogspot.com/-l8YdwfWOEd8/V-InhkX6ciI/AAAAAAAAK-U/wYbFWHhwZ6Ep4_wEh-0lhZP1na6zWn4RgCLcB/s1600/pic1.jpg)  
  
－－－－－－－－－－－－－－－－  
因為一連幾天透過這種方式重溫python程式語法，一邊摸索一邊回想過去讀過的一些資訊很需要再重新拿出來翻讀，以確認自己的觀念與認知正確。尤其雖然只是簡單地引入某些別人早已寫好的函式庫，利用此處整理一下之前從[Learning Python the Hard Way:Modules, Classes, and Objects](https://learnpythonthehardway.org/book/ex40.html)  
Moudle簡單說，可以把它看成一支多支的python 程式，例如寫了一支簡單的mystuff.py 程式，其內容如下：  
  
def apple():  
print "I AM APPLES!"  
  
tangerine = "Living reflection of a dream"  #這裏tangerine和上面的apple不同，前者只是一個變數，後者是一個可執行某種功能的函式  
  
現在在另一支程式中，要使用到apple函式或使用tangerine這個變數  
import mystuff  
mystuff.apple()　　# get apple from the module mystuff.py  
print (mystuff.tangerine) # get  tangerine, it's a variable   


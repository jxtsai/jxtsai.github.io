---
date: 2016-09-23 07:39:00+00:00
title: python Exifread, PIL練習 抽出圖片元數據
category:
- python
---

原文出處：　[http://motherboard.vice.com/read/hack-this-extra-image-metadata-using-python  
](http://motherboard.vice.com/read/hack-this-extra-image-metadata-using-python)  
1) [ExifRead](https://pypi.python.org/pypi/ExifRead%E3%80%80)　  
利用python 函式庫　ExifRead　即可輕易地作 tiff/jpeg 檔案格式的元數據metadata抽取  
先透過PIP安裝好ExifRead函式庫　  
$pip install exifread  
  
直接在CLI命令列執行　EXIF.py，即可對單一照片檔案image1.jpg　來抓出此張照片相關資料數據  
$ EXIF.py image1.jpg  
我以自己一年多前利用手機拍的[這張照片](https://www.flickr.com/photos/a5288/18602753328/)為例  
利用ＥxifＲead函式庫執行上一行指令，傳回來的結果如下：  


<blockquote>Opening: pic.jpg  
EXIF ApertureValue (Ratio): 2  
EXIF ColorSpace (Short): sRGB  
EXIF ComponentsConfiguration (Undefined): YCbCr  
EXIF DateTimeDigitized (ASCII): 2002:12:08 12:00:00  
EXIF DateTimeOriginal (ASCII): 2015:06:13 10:21:45  
EXIF ExifImageLength (Long): 2448  
EXIF ExifImageWidth (Long): 3264  
EXIF ExifVersion (Undefined): 0220  
EXIF ExposureTime (Ratio): 11/20000  
EXIF FlashPixVersion (Undefined): 0100  
EXIF FocalLength (Ratio): 177/50  
EXIF ISOSpeedRatings (Short): 100  
EXIF InteroperabilityOffset (Long): 535  
EXIF UserComment (Undefined): d with VSCOcam  
Image Copyright (ASCII): COPYRIGHT 2015. ALL RIGHTS RESERVED  
Image ExifOffset (Long): 275  
Image GPSInfo (Long): 565  
Image ImageDescription (ASCII): Processed with VSCOcam  
Image Make (ASCII): Xiaomi  
Image Model (ASCII): MiTwo  
Image ResolutionUnit (Short): Pixels/Inch  
Image Software (ASCII): VSCOcam Android Version: v3.3.2 (217)  
Image XResolution (Ratio): 72  
Image YCbCrPositioning (Short): Centered  
Image YResolution (Ratio): 72  
Interoperability InteroperabilityIndex (ASCII): R98  
Interoperability InteroperabilityVersion (Undefined): [48, 49, 48, 48]  
Thumbnail XResolution (Ratio): 72  
Thumbnail YResolution (Ratio): 72</blockquote>

試了另一張別人拍的照片，其中最大的差異應該是拍照者有開啟手機的ＧＰＳ定位，故在其照片的元數據標誌上出現了地理位置的資訊。  


<blockquote>File has JPEG thumbnail  
EXIF ApertureValue (Ratio): 4845/1918  
EXIF BrightnessValue (Signed Ratio): 14515/1629  
EXIF ColorSpace (Short): sRGB  
EXIF ComponentsConfiguration (Undefined): YCbCr  
EXIF DateTimeDigitized (ASCII): 2013:03:09 16:36:20  
EXIF DateTimeOriginal (ASCII): 2013:03:09 16:36:20  
EXIF ExifImageLength (Long): 2448  
EXIF ExifImageWidth (Long): 3264  
EXIF ExifVersion (Undefined): 0221  
EXIF ExposureMode (Short): Auto Exposure  
EXIF ExposureProgram (Short): Program Normal  
EXIF ExposureTime (Ratio): 1/1227  
EXIF FNumber (Ratio): 12/5  
EXIF Flash (Short): Flash did not fire, compulsory flash mode  
EXIF FlashPixVersion (Undefined): 0100  
EXIF FocalLength (Ratio): 107/25  
EXIF FocalLengthIn35mmFilm (Short): 35  
EXIF ISOSpeedRatings (Short): 50  
EXIF MeteringMode (Short): Pattern  
EXIF SceneCaptureType (Short): Standard  
EXIF SensingMethod (Short): One-chip color area  
EXIF ShutterSpeedValue (Signed Ratio): 10343/1008  
EXIF SubjectArea (Short): [1631, 1223, 881, 881]  
EXIF WhiteBalance (Short): Auto  
GPS GPSAltitude (Ratio): 34  
GPS GPSAltitudeRef (Byte): 0  
GPS GPSImgDirection (Ratio): 23341/197  
GPS GPSImgDirectionRef (ASCII): T  
GPS GPSLatitude (Ratio): [22, 1002/25, 0]  
GPS GPSLatitudeRef (ASCII): N  
GPS GPSLongitude (Ratio): [120, 1833/100, 0]  
GPS GPSLongitudeRef (ASCII): E  
GPS GPSTimeStamp (Ratio): [8, 36, 41/2]  
Image DateTime (ASCII): 2013:03:09 16:36:20  
Image ExifOffset (Long): 204  
Image GPSInfo (Long): 594  
Image Make (ASCII): Apple  
Image Model (ASCII): iPhone 4S  
Image Orientation (Short): Horizontal (normal)  
Image ResolutionUnit (Short): Pixels/Inch  
Image Software (ASCII): 6.1.2  
Image XResolution (Ratio): 72  
Image YCbCrPositioning (Short): Centered  
Image YResolution (Ratio): 72  
Thumbnail Compression (Short): JPEG (old-style)  
Thumbnail JPEGInterchangeFormat (Long): 890  
Thumbnail JPEGInterchangeFormatLength (Long): 11733  
Thumbnail ResolutionUnit (Short): Pixels/Inch  
Thumbnail XResolution (Ratio): 72  
Thumbnail YResolution (Ratio): 72</blockquote>

  
當然除了在ＣＬＩ執行EXIF.py外，也可以另外寫一支簡單python的程式碼，引入ExifRead函式庫，以善用其相關method功能。其中.process_file()的功能據稍是：to deal with all the arbitrary nasty bits　of the EXIF standard,什麼意思，我也不太懂，而其回傳的傳是一組dictionary的資料結構。  
  
![]()  
  
2) Pillow 另一個python  函式庫  
之前習作過利用pillow (Python Images Library)進行圖片編修，而這回則是要利用它的  
同樣也是先透過PIP 把它安裝好  
$pip install pillow  
  
TAGS, GPSTAGS 這兩個類別class的使用文件  
http://pillow.readthedocs.io/en/latest/reference/ExifTags.html?highlight=ＴＡＧＳ  
http://pillow.readthedocs.io/en/latest/reference/ExifTags.html?highlight=GPSTAGS  
但其實寫了跟沒寫差不多，　請參考其原始碼內容，以了解這個dictionary各自key/value 之意義  
https://github.com/python-pillow/Pillow/blob/master/PIL/ExifTags.py  
  
照著原作，打入以下的程式碼,會回傳下面的key/ value 對應資訊  
  


<blockquote>  
ExifVersion b'0221'  
ComponentsConfiguration b'x01x02x03x00'  
ApertureValue (4845, 1918)  
DateTimeOriginal 2013:03:09 16:36:20  
DateTimeDigitized 2013:03:09 16:36:20  
FocalLengthIn35mmFilm 35  
FlashPixVersion b'0100'  
MeteringMode 5  
Flash 16  
FocalLength (107, 25)  
ExposureMode 0  
Make Apple  
Model iPhone 4S  
Orientation 1  
YCbCrPositioning 1  
SubjectLocation (1631, 1223, 881, 881)  
SensingMethod 2  
XResolution (72, 1)  
YResolution (72, 1)  
ExposureTime (1, 1227)  
ExifImageHeight 2448  
ExposureProgram 2  
ColorSpace 1  
GPSInfo {16: 'T', 1: 'N', 2: ((22, 1), (4008, 100), (0, 1)), 3: 'E', 4: ((120, 1), (1833, 100), (0, 1)), 5: 0, 6: (34, 1), 7: ((8, 1), (36, 1), (2050, 100)), 17: (23341, 197)}  
ISOSpeedRatings 50  
ResolutionUnit 2  
ExifOffset 204  
WhiteBalance 0  
SceneCaptureType 0  
FNumber (12, 5)  
Software 6.1.2  
DateTime 2013:03:09 16:36:20  
ExifImageWidth 3264  
</blockquote>

  
試著再一行行拆解上面這簡單幾行的程式碼  
from PIL import Image  
from PIL.ExifTags import TAGS, GPSTAGS  
img = Image.open("pic1.jpg")  
print(img)   
#螢幕回傳以下資訊：  
info = img._getexif()　  
print info  
#回傳一組dictionary, 但其key以數字代表，從相應的數值value有些可以猜出它可能代表的東西或標記。如果用下面迴圈的寫法，得出來的內容物一樣，但不是dictionary型態，而是把dictionary每一個對應的key/value一一回傳打印出來。不過還是不知道變數"tag"代表的意義，這裏它仍只是一堆數字標誌的代號。  
for tag, value in info.items():  
print(tag, value)  
另外再試這樣：  
for tag, value in info.items():  
print(TAGS.get(tag)  
這次回傳印出的果然就是tag代表的標記數字意義  
所以我把原文中的程式碼改成：  
for tag, value in info.items():  
key =TAGS.get(tag)  
print(key, value)  
  
透過這次練習，除了學到PIL.ExifTags模組以及ExifRead函式庫。其中又透過PIL.ExifTags　TAGS, GSPTAGS二個類別class，簡單地重溫了一下python資料結構形態[dicitonary](https://docs.python.org/2/tutorial/datastructures.html#dictionaries),以及dictionary[內鍵功能](https://docs.python.org/2/library/stdtypes.html#typesmapping)（如本例中的items()）的進一步認識  
  
最後，作了半天的元數據metadata抽取，到底有什麼意思呢？在表象上我們可看到的資料數據底下，還有這些由機器數位過程所產生記錄下來有關資料的資料。它能夠揭發的資訊，恐怕是原資料當事人也不知道的「自己」。如果你對元數據還是一無所知，不妨看看Pirivacy International 所製作的這支三分鐘小動畫。  
[https://privacyinternational.org/node/573](https://privacyinternational.org/node/573)　

---
author: chihsun.tsai@gmail.com
comments: true
date: 2005-01-22 11:25:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2005/01/22/%e6%9c%ac%e7%ab%99-movable-type-%e9%98%b2%e5%88%b6spam%e9%80%b2%e5%ba%a6/
slug: '%e6%9c%ac%e7%ab%99-movable-type-%e9%98%b2%e5%88%b6spam%e9%80%b2%e5%ba%a6'
title: 本站 movable Type 防制spam進度
wordpress_id: 906
categories:
- blogging
- dotlife
---

timayou.org 站上的幾個blog 系統([mobavle type](http://timayouth.org/umm/archives/2004/12/ece.html#comment58)、[plog](http://www.timayouth.org/plog)、[word press](http://www.timayouth.org/))都開始遭受留言機器人的spams attack。  
在plog 的部份，我已加裝了mark 調製的[留言認證外掛](http://www.timayouth.org/plog/post/1/130)。而在MT部份，原本umm所建議採用的留言安全碼外掛程式，在他辛苦地試了幾次後，卻一直無法正常地顯示安全碼圖像。這部份可能和虛擬主機供應商所提供的GD.pm 模組有關，須要再進一步地檢查嘗試。在此之前，我們還是恢復正常的留言功能，並參考[oui-blog ](http://www.oui-blog.com/archives/2005/01/spamae_aeea.php)上由老猫網友所提供的[「窗口自動檢查法」](http://www.blogfirefox.com/archives/2004/12/movabletypeomme.html)。  
現在，我已弄好了commnents.cgi 的修改，但還須請各位使用mt系統使用者所配合的一道手續是：  
在你個人的網誌組態上去修改「單篇彙整」模版( Individual Entry Archive )  
  
在＜form＞和＜/form＞之間，加上這兩列即可：  
  
   ＜input type="hidden" name="spammer" value="goaway" /＞  
  
   ＜input type="hidden" name="spamming" value="gotohell" /＞  
  
ps. 請注意，""符號須為半形，但在本文中為了顯示於內文，所以用全形替代。  
  
希望這個方法可以暫時堵住spam，另外有關安全碼認證的外掛功能，我和umm會再努力搞定。

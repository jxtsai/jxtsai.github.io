---
author: jx tsai
comments: true
date: 2015-12-29 00:38:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2015/12/29/linux%e5%ae%b6%e6%97%8f%e5%85%a5%e9%96%80-%ef%bc%9a%e8%b5%b7%e6%89%8b%e5%bc%8f-ubuntu/
slug: linux%e5%ae%b6%e6%97%8f%e5%85%a5%e9%96%80-%ef%bc%9a%e8%b5%b7%e6%89%8b%e5%bc%8f-ubuntu
title: Linux家族入門 ：起手式 ubuntu
wordpress_id: 102
categories:
- e-learning
- ubuntu
---

使用的筆電／桌機從Windows [轉換成linux 系統也近一年了](http://self.jxtsai.info/2015/05/ubuntuos-x.html)，雖說是linux，但安裝的ubuntu家族的發行版本，而這版本卻在眾家linux電腦高手眼中視為花拳繡腿，昡華的桌面大量提供圖型介面操作便利，只是一個吸引小孩子們玩的作業系統，沒有好好發揮純文字指令介面技術硬派風格。都已經願意放下長年的習慣投入自由陣營還被這樣嘲笑心裏當然不好受，畢竟是逃開了長年以來被微軟綁架的電腦作業系統環境控制，正想展開另一番自由天地的追尋。或許正面來看這種嘲笑，就是linux之道又廣又深，值得好好多了解linux家族各種版本的差異與合適需求，慢慢累積練就一身功力吧。  
  
後來才知道，除了幾年前linux家族中火紅的ubuntu 版本外，近年來同屬Debian一脈的Linux Mint 更有急起直追之勢。我曾經短暫在ＡＩＯ桌機上安裝過MINT 17版本，它的桌面環境操作感果真有點像windows XP, Vista，初安裝的預設軟體包也比ubuntu 貼心許多，的確是從windows 跳槽linux的優先選項之二。  
  
回到我個人的學習linux的使用之道，先好奇盲目地安裝了ubtunu作業系統，學習在新環境中如何應付自己平日使用電腦常需用到的功能即可，這時候最大的挑戰應該是中文輸入的適應與替代軟體安裝的調適。ubuntu 12.04之後，開始內鍵了「ubuntu software center」，就好似Android手機下的google play 軟體安裝市集，透過它尋找各式需求的軟體一鍵快速進行安裝。這大大解決了早期版本中，只有內鍵「synaptic套件管理程式」，對於新手要安裝或移除軟體多半不知如何正確下手，只能靠誤打誤撞的勇氣和幸運。然而在看似友善「ubuntu software center」軟體安裝庫中，仍然常常找不到早已大受歡迎的軟體，這時候該怎麼辦呢？從網路求救，學會了還有一招叫自定安裝，說穿了就是如何更新第三方軟體庫，然後透過apt-get install 的文字指令安裝更多需要的軟體。學會了這招之後，多少會對終端機下的文字指令操作有點信心，此時可以再搭配找本電腦教科書，進一步深入了解如何以文字指令介面環境簡單修改一些檔案下的環境配置或是檔案刪。除了市面上常見的ubutnu入門書外（不一定要花錢買最新版，從圖書館借來翻翻即可），不妨可以上上Linux　Foundation 在EDx開設的免費入門課程：[ Introduction to Linux](https://www.edx.org/course/introduction-linux-linuxfoundationx-lfs101x-2)。  
  
![Introduction to Linux](https://image.slidesharecdn.com/introductiontolinuxpptbatch2-141025005514-conversion-gate01/95/introduction-to-linux-ppt-3-638.jpg)  
  
從這堂入門課程中，我才開始對Linux家族各自發展的不同發行版本有了一點基本的認識，也在這樣認知基礎上，打算來試玩其它發行版本的linux系統，以更了解其間的差異與優劣。擬試的第一個版本，就是CentOS，不只因為聽說網路上許多伺服器系統都是以它為作業環境，在我另一台少用的[樹莓派小電腦](http://self.jxtsai.info/2015/06/blog-post_19.html)，即是以CentOS為基礎打造的作業環境，理應於我不至於太困難才是。再者，過去我所接觸過的網路伺服器環境，多半是由Apache架構起來，安裝php/ MySQL／HTML的網路環境，但是如何使用安裝其它一些「較新」的網架開發架構（如Ruby on Rail/ Python: Dijango ），看來得先了解它背後的作業系統環境才是。  
  
有了安裝ubuntu 經驗，如何安裝CentOs／Federa 看似不是大問題，反正就是先到其官網下載合適自己電腦硬體配置的鏡像燒錄檔，製作成開機光碟或開機USB。而在CentOS官網提供使用者不同用途需求的版本中，為圖省空間和時間，我先下載了Minimal　ISO，沒想到反而讓我誤打入Linux純文字指令介面的真正修羅道場啊。

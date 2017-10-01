---
author: jx tsai
comments: true
date: 2015-02-20 16:51:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2015/02/20/%e5%9c%a8ubuntu%e4%b8%8a%e5%ae%89%e8%a3%9d%e5%a5%bdruby-on-rails/
slug: '%e5%9c%a8ubuntu%e4%b8%8a%e5%ae%89%e8%a3%9d%e5%a5%bdruby-on-rails'
title: 在ubuntu上安裝好ruby on rails
wordpress_id: 183
categories:
- e-learning
- ruby
- ubuntu
---

幾年前像瞎子模象地學想Ruby on rails,不明就理地在 windows 作業系統下安裝該程式的開發環境。  
  
近來得閒又開始學習一些有的沒的電腦程式語言後（當然還是懞懞懂懂半知無解的狀態），心想應該差不多可以再把ruby on rails重新找出來再自習一下，也許這次會更懂一點？  
  
不過要開始學習這套程式語言，第一件事就是得在電腦上安裝好ruby on rails的開發環境。因為目前主要使用的電腦以ubuntu為主，便查一下如何在其上安裝ruby on rails。google跑出來的第一則網頁「[Setup Ruby On Rails on Ubuntu 14.10 Utopic Unicorn](https://gorails.com/setup/ubuntu/14.10)」開宗明義在第一行就告訴使用者，安裝過程大約要花30分鐘，讓我頓時失去勇氣，想說那就還是回頭先以windows作業系統下的安裝為先。結果參考ruby installer 官網的操作，雖然是把ruby 和rail 都裝起來了，但是開始學著寫程式時，卻遇上javascript問題，目前還不知道如何解決。  
  
於是回過頭來橫下心要來搞定在ubuntu 上的安裝，仔細跟隨「[Setup Ruby On Rails on Ubuntu 14.10 Utopic Unicorn](https://gorails.com/setup/ubuntu/14.10)」這篇文章的步驟，選擇了「 rbenv.」的方式，過程還算順利，除了在步驟二：Configuring Git（別忘了要先有GitHub帳號），如何生成SSH key時有點疑惑，這時要記得先登入GitHub帳戶，然後當terminal 出現 Enter file in which to save the key 時，直接按下「enter」，同時在詢問Enter passphrase，我也是按「enter」省去麻煩 。完成上述後，再按原網頁指示的，在terminal鍵入： cat ~/.ssh/id_rsa.pub  
就會自動生成了SSH key，把這些奇怪的東西貼到自己GitHub帳戶底下的SSH key就可以了。  
(以前不知道ubuntu 下操作ternimal界面，該指令可以用「貼上」的方式，省得自己打一長串不明白其意義，又常會掉字拼錯的東西)  
  
在第四個步驟：設定資料庫時，我選擇了MySQL的安裝（所以可以不用理會Setting Up PostgreSQL那一段），也設定了自己root帳戶的資料庫權限密碼，故最後一個步驟是教導使用者在已完成所有ruby on rails的開發環境下，開始製作自己的第一支程式，且如有必要，得修改連結資料庫檔案的root帳戶密碼，才可讓新産生的程式可以順利連結存取MySQL資料庫。  
  
嗯如果我這之前沒有先重溫windows上的操作（雖然結果是失敗的），大概最後一個步驟也不會看懂它的意思，很可能就卡在那裏了。

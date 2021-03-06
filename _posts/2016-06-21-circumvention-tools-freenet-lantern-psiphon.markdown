---
author: jx tsai
comments: true
date: 2016-06-21 09:31:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/06/21/%e4%b8%89%e6%ac%be%e7%b6%b2%e8%b7%af%e7%bf%bb%e7%89%86%e5%b7%a5%e5%85%b7-freenet-lantern-psiphon/
slug: '%e4%b8%89%e6%ac%be%e7%b6%b2%e8%b7%af%e7%bf%bb%e7%89%86%e5%b7%a5%e5%85%b7-freenet-lantern-psiphon'
title: 三款網路翻牆工具--freenet, lantern, psiphon
wordpress_id: 60
categories:
- e-learning
- localization
- opensources
---

這一年多來，偶而幫Open Technology Ｆund 放在transifex.com上的公開專案進行正體中文化的翻譯。如果我沒理解錯誤（知道正確資訊又剛好有看到這篇文章者煩請指正），ＯＴＦ有部份資金來自Ｒadio Free Asia，而ＲＦＡ這個由美國官方資助的公共媒體的確有不少來自美國政府部門的經費支援。不過我要說的是ＯＴＦ所支持與投入的數位科技專案，多是以協助在資訊封閉不自由的地區、社會、國家如何透過數位技術科技的開發和應用，打斷資訊的隴斷控制。於此同時ＯＴＦ另一關注的重點則是如何保護人民在使用工具獲取資訊時，不會受到權力者（主要是政府部門）的監控干擾。  
  
剛好這兩個議題算是我個人比較有興趣的，所以也用了一些時間在相關軟體的中文化與介紹上。而今天要一口氣介紹的三款網路翻牆工具，我都有幸（嗯其實是沒有人和我搶）參與了其正體中文化的進行，當然其中也不少是借力於先行完成的簡體中文稿的基礎。  
  
簡單說明，所謂翻牆工具是為了對付網路的審查與封鎖。因此不能不先了解到底何謂**「網路審查與封鎖」**？網民們或多或少知道中國ＧＦＷ的威力以及其對許多境外跨國網站的封鎖政策，我就不多說。自詡為進入民主待深化、人權保障雛備，甚致有人覺得言論太過自由的今日台灣，是否仍然存有網路審查與封鎖的現象呢？答案是：**當然有！！！**。只是在中國執行「「網路審查與封鎖」」的權力者其無法相應的監督和制衡，而在台灣稍慶幸言論資訊被審查而遭移除的原因與手段多少有點法律正當性的依據，例如以未成年者身心發展健康為由，在校園內的公共電腦透過關鍵字設定而無法連到色情網站、臉書接受用戶檢舉認同女性身體上空照片有色情暗示而移除該貼文或暫時停止張貼者使用、毀謗侮辱他人或內容侵犯著作權遭當事人向網管反應在未經法院審理之前內容已被移除.......  


<blockquote>許多政府、公司、學校與公共網路使用區都透過一些軟體來阻止使用者連上某一些網站或網路服務。這樣稱之為網路過濾或是封鎖，也被視為網路審查的一種。內容過濾來自不同的形式.有時整個網站都被封鎖有的只是包含某些關鍵字的內容被過濾.某個國家或許會封鎖了整個臉書網站，有些則是封鎖臉書上部份的社群小組或是含有某些字眼的網頁內容。不管其內容是如何被過濾封鎖，你只有透過一些對付工具才能取得資訊. 對付因應的工具往往透過分散你的網路或透過其它電腦的繞行交通，以躲避執行審查的機器。現有許多對付網路審查的工具，有些提供多出來的安全層帶供你使用。這樣的工具最適合受到威脅的用戶。</blockquote>

（摘自Security First umbrella_app:網路初學者介紹篇communications the internet beginner ）  
  
繼續根據umbrella_app網路初學者介紹篇的整理，一般而言要突破網路封鎖所採的方式可歸類至少有三種方式：  
  
１)網站差異:試圖找另一個替代的網域名或網址.以推特為例, 你可以造訪它的行動網址http://m.twitter.com來取代http://twitter.com. 審查者封鎖網站或網頁往往依照被禁止的黑名單資料,所以不在名單上的網址或許可以躲過一劫,因為他們並不知道某一個特定網站有其它不同的網域名稱,尤其是因為遭封鎖而註冊了其它的網域名.  
  
２)網頁代理器 (例如 [https://proxy.org/](https://proxy.org/))是最簡單對付審的方式之一.它是由網站讓用戶可以近用其它遭到封鎖的網址. 使用網頁代理,你只需在其網頁上的輸入框打上被過濾的網址，代理器就會在網頁上呈現出你要求的內容。網頁代理器是一個快速近用封鎖網站的好方法,但是它也有一些缺點：a)它住往無法提供安全保密，如果你的網路行為受到監控的威脅,這就不是一個好的選項。b)有時這個工具也無法提供你要求的正確網頁內容，許多網頁代理無法承載複雜的網站，像是有影音內容的網站。c)如其名稱所示網頁代理由能提供網站服務，你無法利用它來使用即時通訊或是電子郵件程式。d)最後,網頁代理本身也給使用者帶來一些風險，因為代理器會全程記錄你的瀏網行為。有一些代理服務使用了加密功能可以提供多一層的安全防護以及躲避過濾。雖然它的連線有加密但是服務提供者仍然保有你的網路資料，這意謂著它並不是匿名。不管如何，這總是稍比一般性的網頁代理更為安全.最簡單形式的加密網頁代理是透過使"https"開頭的網址，它的網站會使用加密通訊。  
  
3)虛擬私人網路 (VPN)會在你的電腦與其它電腦之間進行加密與傳送。這個電腦可以商用或是非營利,或是由你的公司或是一個信賴者所架設的VPN 服務。代理伺服器只有網頁交通功能，但是VPN可以加密和保護通訊內容。主要的差異就在 VPN伺服器可以加密資料，而代理器則不能。VPN也可以讓你方使使用更多網路資源，例如透過它讀取網頁、電子郵件、即時通訊、網路電話等種種服務。不要使用不信任的VPＮ：VPN透過本機上的加密保護你的使用記錄，但是VPN提供者仍然可以保留你訪問過的網站活動記錄甚致將其提供給第三方以直接窺探你的瀏覧歷史。依照你受威脅模式的程度，政府很可能監聽或是取得你的 VPN 記錄，這將是很大的風險。  
  
當然可以用來突破網路審查（這裏指的是網站被封鎖無法連上的情況，而非內容被移附）工具應該不少，因透過中文化工作，有機會稍接觸的三種翻牆連網工具簡介：  
  
１）　[Freenet](https://freenetproject.org/)：中文稱「自由網」，根據其官網上的介紹，「它是一個分散式、非中心化的資訊儲存與存取的系統。系統的目標是要在Internet上可以自由地傳遞各類資訊，而不會受到任何控制。要達到這個目標，就是提供匿名的方式來置放資訊到Freenet上，並且透過Freenet來存取其他Internet資訊。」我個人感覺這個是三個軟體中最複雜神祕的一套，其作用不只是在突破網站封鎖，還得把自己的電腦變成自由網中的一個節點，並劃出自己部份硬碟與流量來做為儲存分享交換「檔案」的空間。有技客利用它來連上DarkNet、Deep Web（暗黑網絡、隱形網絡或深層網絡。泛指一些不能由傳統搜尋器找到的網站，須通過動態請求或由特定的瀏覧器才可找到）  
  
２）　Lantern: 中文被譯成「藍燈」。它似乎也有應用到點對點之間的技術，軟體會自動檢測一個網站是否被封鎖。對那些被封鎖的網站，Lantern 通過自有的服務器或者未封鎖地區的用戶運行的 Lantern 來提供訪問。如果網站沒有被封鎖，Lantern 選擇靠邊站。這樣瀏覽器就會直接訪問網站，而速度不受影響。  
  
３）　Psiphon： 中文被譯成心「賽風」，是一個以VPN-為基礎的工具但也混合利用了SSH, HTTP Proxy等技術，以代理使用者所有的網路交流，不只限於網頁瀏覧。使用安裝請參考之前[umbrella app 工具指南介紹](https://www.jxtsai.info/blog/archives/2666)。  
  
作了一張簡表來比較這三種軟體的特色。也許因為相對地幸運活在今日台灣，所以沒怎麼能親身比較它們各自的優缺點在哪裏，只能先以官網開發者提供的基本資料作介紹。  
![circumvent](https://3.bp.blogspot.com/-uAoTnenTgVI/V30cucnNWDI/AAAAAAAAKPc/094zrXMj-w0nMUFwGmE_KKdfSjrhSS_3QCLcB/s1600/circumvent-1-667x1024.png)

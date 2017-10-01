---
author: jx tsai
comments: true
date: 2016-05-14 10:49:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/05/14/jitsi-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97/
slug: jitsi-%e5%b7%a5%e5%85%b7%e6%8c%87%e5%8d%97
title: JITSI 工具指南
wordpress_id: 80
categories:
- human rights
- localization
- opensources
- Security First
- umbrella app
---

本文同樣是[Security First umbrella app](https://secfirst.org/) 中文化的系列初稿。作這種中文化真的是一件超級無趣與累人的過程，尤其是當某一些軟體本身根本在華文社區中未受到重視，沒有在地語言包，都讓我懷疑投入只是介紹工具的中文化是否真能推動一些自由軟體與安全通訊更易被接受和使用呢，還是根本該再進一步自告奮勇地來作軟體本身的中文語言包（真是夠了）。Jitsi是一套重視通訊安全與私密者可以考慮的軟體工具，或許它永遠都不會是主流，但至少提供了另一種偏好的選擇。（為了解jitsi的操作介面，我也申請了一個SIP帳號：jxtsai@ostel.co來試用，雖然電腦與手機的即時通軟體/VOIP這幾年我很少很少有機會用幾乎不會打開）  
  
***本文為Security First製作的手機應用umbrella app正體中文化翻譯系列資料之一。目前仍為初稿狀態，虛心接受指正批評。原始的json資料格式配合app電子書的html編輯標籤，轉貼到部落格上排版混亂也欠缺原始圖檔請見諒。***  
  
**Jitsi 工具指南:**安全的語音、視訊與即時通訊軟體  
![jitsi](https://3.bp.blogspot.com/-eAcjRCU791c/V35FNMU7nAI/AAAAAAAAKVo/GojV5HzNC5UR5voaEFwqIxx3QH3AsoJZwCLcB/s1600/jitsi-sip-client.png)  
  
學習內容: [撥打電話](umbrella://lesson/making-a-call)  
下載地點:[https://jitsi.org/Main/Download](https://jitsi.org/Main/Download)  
電腦需求:Windows, Mac OS X, Ubuntu, Linux等作業環境  
本指南中所用的軟體版本:Jitsi 2.4  
版權宣告:免費開源軟體  
程度:初學者  
所需時間:15-20 分鐘  
**  
1.1 開始啟動**  
使用Jitsi可讓你:替代Skype進行電腦之間安全加密的語音通話、簡訊傳送以及視訊會議.  
它可以登入且利用你已有的通訊服務帳號，如 Facebook, MSN, Google Talk， Yahoo Messenger等，同步與不同頻道的聯絡人通訊.它可以與我們所介紹的其它軟體共用，如Pidgin, Adium and ChatSecure同步進行安全通訊.  
  
**2.1 如何安裝Jitsi**  
要安裝Jitsi, 請執行以下步驟:  
第1步.雙擊所下載的檔案（例如windows系統使用的jisi-2.4-latest-x86.exe) _打開檔案時 - 會自動彈出安全警告視窗_.然後點選「下一步」來啟動 _Windows 安裝_畫面, 它接著會出現 _歡迎來到Jitsi 簡單安裝視窗_.  
第2步.點選「下一步」來激活_末端用戶使用版權絛款_ 視窗; 點選 _接受服務協議_選項以進行_下一個步驟_繼續點選「下一步」以進入檔案安裝的_資料夾目的地_視窗.  
第3步.選擇「下一步」以啟動 _其它任務_然後目前先同意軟體預設的設定.  
**注意:** 當電腦重新開機後，打開「自行啟動」_Auto-start功能可能會讓電腦的速度變慢_, 尤其當你的電腦上有多個應用程式設為自行啟動狀態.  
第4步.點擊「下一步」進入_準備好安裝Jitsi_視窗, 然後點選「安裝」即會啟動 _ Jitsi安裝中_畫面並顯示目前的安裝完成進度.  
第5步.點擊「完成」以結束安裝手續即會自動開啟**Jitsi** 首先會出現_登入_畫面如下:![](http://self.jxtsai.info/%5C%22tool_jitsi1.png%5C%22)  
**注意:**有點時候安裝與第一次啟動Jitsi後，電腦會彈出_「安全警示」視窗 _ 其情況如下圖.  
第6步.同時選擇**私密Private**與 **公開Public**網路二個選項，再點擊_同步取用Allow access_*** 可以看到_Jitsi 登入視窗_或是主要的用戶使用介面視窗.![](http://self.jxtsai.info/%5C%22tool_jitsi2.png%5C%22)  
  
**2.2 如何在Jitsi新增帳號**  
請注意即使Jitsi有使用加密, 網路通訊服務的提供商如Google、Facebook仍然會監控你的通訊(也包括你所通訊的對象), 也會和第三方分享如政府或私人公司這些資訊. 因此儘管Jitsi有加密功能，最好還是避免使用這些服務來做敏感議題的通訊.  
  
**2.2.1 如何新加入Gmail/Google帳號**  
注意:以下以 Google Talk 帳號為例來說明安裝過程,其它的通訊協議安裝也是大同小異 。不同的通訊協議服務提供商之間某些通訊或加密的功能或許會失效 (如 Facebook, Gmail, Yahoo, 等等.). 但基本上同一個服務提供者不同帳號之間的通訊應該還是沒問題.  
第1步.選擇啟動Start > Jitsi或是雙擊桌面上的Jitsi 圖示來開啟應用軟.  
第2步.在_登入_畫面下, 輸入你的Gmail帳號的用戶名稱和密碼, 依下方的圖像所示:![](http://self.jxtsai.info/%5C%22tool_jitsi3.png%5C%22)  
注意:你可以同時使用不同聊天服務協議並新增多個帳號.  
**第3步.** 點點「登入」以激活你的即時聊天視窗.  
注意:如果你關閉 _登入_視窗，或是你需要新增其它的帳號，你可以在 **_檔案下File > 新增其它帳號..._**.  
在新出現的視窗中選擇**「網路」Network**為_Google Talk_ 然後再打入Gmail 帳號的用戶名稱與密碼，一如下圖所示:![](http://self.jxtsai.info/%5C%22tool_jitsi4.png%5C%22)  
要在Jitsi上認證你所註冊的Gmail 帳號, 請依照以下步驟:  
第1步.在選單下「選擇」Select **「工具」Tools >「選項」 Options** 以出現以下視窗:![](http://self.jxtsai.info/%5C%22tool_jitsi5.png%5C%22)  
注意:如果你用的是二步驟認證方式以保護你Gmail帳號的取用, 當你試著透過Jitsi 以一般密碼來登入Gmail帳號時，你可能會收到如下的訊息. 要登入Jitsi, 你得要產生一組「應用程式專用」密碼. 請Google's [的說明指示來進行](https://support.google.com/accounts/answer/185833?hl=en)  
  
**2.2.2 註冊新的Jabber/XMPP 或 SIP 帳號或是把已有帳號加到Jitsi**  
Jabber/XMPP 、SIP 開放標準的文字與聲音通訊. 有許多伺服主機提供免費的帳號申請好讓你使用Jitsi. 下面我們推薦一些適合作敏感通訊使用的服務主機  
Riseup.net Jabber/XMPP account  
如果你有Riseup.net 安全電子郵件服務的帳號 (主機位於美國) 你也可以利用在Jisti底下加入這個帳號來進行Jabber/XMPP 網路通訊 -請見下面如何新增已有Jabber/XMPP 帳號的介紹.  
**Jabber.ccc.de**其它Jabber/XMPP 帳號  
你依以下步驟在Jabber.ccc.de 註冊帳號 (其主機位在德國):  
Step 1.Jitsi選單底下, 選擇「檔案」File > Add新增新帳號 .... 在新彈出的視窗中, 選擇**_「網路」Network:_ XMPP** 然點圈選_「創建新的」Create a new XMPP account*** 選項_. 在伺服器位置上 _*Server_, 打入　jabber.ccc.de　再輸入你想取的XMPP 用戶名稱以及 _密碼_然後按密碼欄位的_確認鍵Confirm_，它就會出現以下畫面:![](http://self.jxtsai.info/%5C%22tool_jitsi6.png%5C%22)  
**第2步.** 點擊 **「新增」Add**. 在成功註冊後你將可以看到一個類似以上的畫面.  
如果你想要的用戶名稱已被使用, 註冊過程將會失敗而出現以下訊息_由於以下錯誤訊息我們無法創建你的帳號:無法確認資料_.你可以試著用不同的用戶名稱再重新一遍註冊過程.  
**注意**如果你超過12個月未登入jabber.ccc.de，你的帳號將自動遭到移除而你的用戶名稱也可能被其它人選用.  
**ostel.co** SIP 帳號  
**SIP** 帳號無法透過Jitsi軟體來進行註冊. 這個 **ostel.co** 伺服器(主機位於USA) 提供[用戶在其網站上註冊](https://ostel.co/users/sign_up). 輸入你要的用戶名稱,密碼以及一組你現有的電子郵件，然後 點擊網頁上的_「註冊」Sign up_按鍵. 順利完成註冊後再回到Jitsi . 在選單中選擇在**_「檔案」File >「新增帳號」 Add new account..._**, 選擇 **「網路」Network: SIP**,然後打入之前在網頁上申請的用戶名稱(例如： terence.the.tester@ostel.co) 以及密碼，再點擊**_「新增」Add_**. 請見下面的參考圖片:![](http://self.jxtsai.info/%5C%22tool_jitsi7.png%5C%22)  
**新增已有的Jabber/XMPP or SIP 帳號到 Jitsi**  
如果你之前已有Jabber/XMPP 或 SIP 帳號，你可以把它們加到 Jitsi，在選單下選擇**_「檔案」File >「新增帳號」 Add new account..._**然後再選擇適合的網路協議服務 (依 XMPP or SIP 等帳號類型而定).  
  
**2.2.3 如何加入Facebook帳號**  
首先你得在Facebook上完成二項設定變更才能讓Jitsi可以串結你的Facebook 聊天協議.  
**Facebook 用名名稱**  
Facebook 要用一個用戶名稱來連結到Jitsi以便使用其聊天功能.大多數旳臉書用戶已有其用戶名稱.要查出你的用戶名稱,請登入自己臉書帳號:你的用戶名稱正是當你檢視自己的時間表或頁面時，　出現於網址列之中出現於 _https://www.facebook.com/_ 之後的名字. 你的用戶名稱也會顯示在你的Facebook個人電子郵件地址(ex: username@facebook.com). 你可以看見或是變更這個用戶名稱，其作法是到你的臉書_「帳號設定」Account Settings > 「一般」General_ 之處或是網址處打入[https://www.facebook.com/username](https://www.facebook.com/username). 設定用戶名稱Facebook 可能會要求你的帳號進行認證，其步驟要求傳送認證碼簡訊到你的手機上.  
**App Settings應用程式設定**  
Facebook的應用程式平台必須先開啟，這樣**Jitsi**才能夠連結到Facebook聊天功能.到你的臉書 _「帳號設定」Account Settings >「應用程式」 Apps_底下檢其設定是否開啟.它將打開你帳號下的"應用程式平台".  
**注意** that啟動了臉書的 "應用程式平台" 也會把你個人的臉書資料開放給其它第三方的應用程式開發者. 這些資料並不只有供你自己同意的臉書應用程式來使用, 也會包括許多你朋友所使用的臉書應用程式. 因此在打開了臉書的 "應用程式平台"之後,也記得要檢查 "Apps others use"「其它應用程式使用」底下的設定. 這個設定可讓你向臉友使用的應用程式隱藏某一些個人資料.不幸的是, Facebook並未提供全盤的個人資料隱藏方式. 某些類別的資訊，(例如朋友清單, 性別, 或是其它你設為公開的資訊)都可以被看到，只要你開啟了Facebook的 "應用程式平台application platform". 所以你可以決定是否要接受這樣的隱私交換.  
現在你可以準備在Jitsi加入你的臉書帳號了. 請依如下的步驟:  
**第1步.** 由主選單下選擇**_「檔案」File >「新增帳號」 Add New Account..._**  
**第2步.** 在新增帳號的對話視窗中,在**「網路」Network**選單中挑選_Facebook_,然後輸入你的用戶名稱和密碼再點擊 **「新增」"Add"**![](http://self.jxtsai.info/%5C%22tool_jitsi8.png%5C%22)  
  
**2.3 如何更改Jitsi帳號的密碼**  
知道如何變更帳號的密碼是一個重要的安全要素. 許同用於Jitsi的帳號在設定下提供了密碼更新的方式, 其可以透由網頁介面來進行.但是有些 Jabber/XMPP與SIP 帳號沒有任何網頁介面可以來管理密碼更新. 要變更這些運行於Jitsi的帳號密碼請依以下步驟:  
**第1步.** 在選單下選擇**_「工具」Tools >「選項」 Options_**,再選擇 **_「帳號」Accounts_**分頁  
**第2步.** 點擊 **_下方的「編輯」Edit_**鍵以激活新視窗.  
**第3步.** 點擊**_「改變帳號密碼」Change account password_ 來激活_變更帳號密碼_視窗.  
**第4步.** 重覆輸入二次新密碼後點選**_「確認鍵」OK_**然後關閉視窗.  
**第5步.** 關閉簡易帳號註冊視窗.**  
  
**2.4 如何設定 Jitsi 以提高其安全性  
2.4.1 取消與移除所有的通話和聊天記錄**  
Jitsi原則會預設儲存語音通話、文字聊天的記錄. 你可以點擊Jitsi 主視窗中的圖示來取用語音或視訊通話資料:![](http://self.jxtsai.info/%5C%22tool_jitsi9.png%5C%22)  
若要看文字聊天記錄則可以到聊天視窗中點擊聯絡人底下一個像是計時器的小圖示:![](http://self.jxtsai.info/%5C%22tool_jitsi10.png%5C%22)  
即便你用OTR方式加密了所有聊天的內容，但你送出或收到的文字訊息仍然會以開放文字格式存在你的電腦上.  
要防止Jitsi收集這些資訊 (以及移除已累積的資料),你和你的聯絡人應該要採取以下步驟.  
**取消Jitsi收集資訊的功能:**  
**第1步.**在選單下選擇**_「工具」Tools > 「選項」Options_**, 選擇**_「一般」General_**分頁然後取消 **_「記錄聊天資料」Log chat history_**的選項.  
**第2步.** 在_「選項」Options_ 視窗下, 首先選擇 **「進階」 Advanced**分頁, 然後再**選擇_「活動記錄」Logging_**部份,**取消_「封包記錄」packet logging_**選項，其如下圖所示:![](http://self.jxtsai.info/%5C%22tool_jitsi11.png%5C%22)  
要重啟Jitsi這些變更才會生效.  
**要移除你過去的通話與聊天記錄:**  
**第1步.**關上Jitsi.  
**第2步.** 到Jitsi使用者資料夾_history_ver1.0_底下移除全部記錄資料.如果你只要消除某一部份的記錄，你也可以移除 _history_ver1.0_的子目錄.至於_「使用者檔案」user profile_ 的位置與_活動記錄資料夾log history_ 依電腦作業系統而異:  
在Windows XP或更早版本上, 它位於_C:\Documents and Settings\<Windows login/user name>\Application Data\Jitsi\history_ver1.0_  
在 Windows Vista, 7, 8, 則是 _C:\Users\<Windows login/user name>\AppData\Roaming\Jitsi\history_ver1.0_  
Mac OS X: 在你的家目錄下 _~/Library/Application Support/Jitsi/history_ver1.0_  
Linux: 在家目錄下 _~/.jitsi/history_ver1.0_  
參見 [安全刪除課程](umbrealla://lesson/safely-deleting%5C)以了解如何安全地移除資訊.  
  
**2.4.2 在文字聊天時使用私密傳訊**  
當你設定好Jitsi後，一般也建議盡可能採用私密與利用OTR加密的通訊方式. 其作法是,在選單下選擇 **_「工具」Tools >「選項」 Options_**,再選擇 **_「安全」Security_**分頁中的**_「聊天」Chat_子分頁並點選啟用幕下方的**_「要求私密傳訊」Require private messaging_** 功能.**  
**  
2.4.3 利用主密碼來保護你的帳號密碼**  
最好不要讓Jitsi記住你帳號的密碼. 如果讓它記憶帳密,任何取用你電腦的人都可以輕易地開啟Jitsi然後登入你的帳號. 它也可能在「選項」視窗中看到你的密碼. 所以**強烈建議**使用好的主密碼來保護你的帳密.一旦你設定好主密碼, Jitsi在啟動後會詢問你.  
**第1步.**在選單中開啟「選項」視窗其方式是先選擇**_「工具」Tools >「選項」 Options_**,再選擇 **_「安全」Security_**分頁下的**_「密碼」Passwords_**子分頁,然後點擊 **_「使用主密碼」Use a master password_** 以激活**_主密碼_**之視窗.  
**第2步.** 在新視窗下,輸入你的主密碼. 如何挑選一組強度高的密碼,請見**[密碼課程](http://self.jxtsai.info/)**.  
**第3步. 點擊 _「確認」OK_**以確認此密碼並激活視窗 彈出**_「主密碼已成功設定」Master Password successfully set up_之訊息**. 點擊 "**OK" 關閉視窗後再重新回到 _「選項」Options_ 視窗其顯示如下圖:**![](http://self.jxtsai.info/%5C%22tool_jitsi12.png%5C%22)**注意:** 改變 **_主密碼_**按鈕可讓你更新主密碼而**_「儲存密碼」Saved Passwords..._**鍵則是讓你可以取用Jitsi 所記住的密碼也可以在需要時移除它們.  
  
**Jitsi - 新增聯絡人以及文字與語音通訊  
3.1 新增聯絡人 (buddies) 到Jitsi**  
在Jitsi下至少有了一組聊天通訊帳號登入後, 你就可以開始新增聯絡並與他們通訊了.  
**第0.步** 在主視窗下選擇**_「開始」Start > Jitsi_** 或是雙擊電腦桌面上的Jitsi圖示以啟動.  
**第1步.** 選擇 **_「檔案」File >「新增聯絡人」 Add contact..._**後將會啟動如下圖的視窗畫面 :![](http://self.jxtsai.info/%5C%22tool_jitsi13.png%5C%22)  
**第2步.** 選擇你要在哪一個聊天帳號下新增聯絡 (例如：_terance.the.tester@jit.si_).  
**可選擇的:** 你也可以新增聯絡人到其它聊天帳號的群組中. 但是,首先你必須先創建一個群組. 從選單下選擇**_「檔案」File >「創建群組」 Create group..._** ).  
輸入聯絡人的用戶名稱或電郵資訊到**_「身份」ID 或「電話號碼」 Number_** 欄位中(例如, _sally.the.doer@jit.si_).  
你可以選擇對方的名字或匿稱,其可見於Jitsi 主視窗的聯絡人清單; 將它鍵入在 **_「顯示名稱」Display name_** 的欄位裏.**第3步.** 關上 _「新增聯絡人」視窗Add contactJitsi主視窗點_點擊「新增」Add_ . 在你的聯絡人清單上你將會看到所新增的聯絡人正處於等待授權的狀態"Waiting for authorisation".  
**第4步.** 一旦當你的聯絡人登入帳號後 (sally.the.doer@jit.si) , 她會收到一個彈出的通知表示你請求把她加入你的聯絡清單:  
對方可以選擇_「忽視」Ignore_這樣你會一直處於等待被授權的狀態， _「拒絕」Deny_, 你將會收到請求遭拒的通知;或是_「授權」Authorise_, 對方已同意你的請求加入所以在你的聯絡清單上可以見到對方._  
  
**3.2 文字聊天 OTR 加密(即時訊息)**  
現在你可以新增聯絡人或是同意它人的授權請求,你可以在聯絡清單上點擊對方名字底下相關的圖示來閧啟文字通訊、視訊或視訊電話、桌面分享等功能:![](http://self.jxtsai.info/%5C%22tool_jitsi14.png%5C%22)  
第1步. 我們將採索Jitsi最主要的功能 :安全文字聊天 、採用OTR加密訊息. OTR的功能類似於我們在本書其它課程中所提到的 GPG/PGP方式. 就如同PGP, 你和通訊者對象可以加密雙方的通訊之前，你們都要先設定好Jitsi以　產生你們的密鑰.在選單下選擇 **_「工具」Tools >「選項」 Options_**然後再選擇**_「安全」Security_**分頁下的**_「聊天」Chat_**子分頁. 你將會看到一個類似底下的畫面:![](http://self.jxtsai.info/%5C%22tool_jitsi15.png%5C%22)  
**第2步.** 再來,請點擊**_「產生」Generate_**鍵. 結果你將會看到生成的指紋碼:![](http://self.jxtsai.info/%5C%22tool_jitsi16.png%5C%22)  
  
每一個帳號會有一組指紋碼.你只需要在新增帳號或是安裝Jitsi進行這個動作，不要把現存的指紋碼移入其它設備上.  
現在你可以進行通訊了:  
**第3步.**從Jitsi 主視窗中選擇一名聯絡人後點擊_「傳送訊息」send message_ 圖示 (聯絡人名字底下左邊算來第一個) 以打開文字聊天視窗:![](http://self.jxtsai.info/%5C%22tool_jitsi17.png%5C%22)  
注意_用OTR的加密聊天_圖示,即為出現在聊天視窗右上方的位置. 這個圖示將提醒你目前的聊天是否處於加密的狀態. 例如現在這個小鎖是打開的(在鎖頭與鎖身之間有一個小空隙!).  
**第4步.**點擊**_OTR加密聊天_**圖示.留意視窗圖示的變化:![](http://self.jxtsai.info/%5C%22tool_jitsi18.png%5C%22)  
觀察到現在鎖已經完全關上了.這表示你和聯絡人之間傳送的任何訊都會被加密. 留意這個訊息仍是_「未查證的私密」unverified private_談話，你應該要 _「授權」authenticate_ sally.the.doer@jit.si.  
**第5步.** 點擊授權連結 **_authenticate sally.the.doer@jit.si_** 來開啟 _「同意友人」Authenticate Buddy_之視窗:![](http://self.jxtsai.info/%5C%22tool_jitsi19.png%5C%22)  
注意它會出現訊息建議你們雙方要透過其它管道(非目前所用的文字聊天)來比對指紋碼 . 這樣你才能更確認所通訊的聯絡人的確是你要找的當事人。比對指紋碼的好方式是當面進行或是透過視訊、聲音等較簡單方式來確認其它人的身份. 完成指紋碼比對後, 從拉下的選單中挑選**_「我已完成認證」I have verified_** 指紋碼的選項，然後點擊**_「授權好友」Authenticate Buddy_**:![](http://self.jxtsai.info/%5C%22tool_jitsi20.png%5C%22)  
關上_「授權好友」Authenticate Buddy_ 視窗以回到聊天主視窗.![](http://self.jxtsai.info/%5C%22tool_jitsi21.png%5C%22)  
留意到現在小鎖圖示不再顯示橙色三角形與白色驚嘆號的危險標記。這表示已授權了你的聯絡人. **每一位聯絡人須要作一次授權的動作.** 如果三角危險標記又再次出現, 它表示你正在與一位未經授權者聊天. 這種情況會發生在你的聯絡人在其它設備上安裝了Jitsi並使用不同的加密鑰匙(重安裝Jitsi或其它 OTR 程式等等).這種情況下你要雙方重新授權以確認彼此通訊對像的身份.Jitsi 可讓你同時與多人文字聊天，但OTR加密只能在一對一時有效.  
  
**3.3 ZRTP 加密的語音與視訊聊天**  
Jitsi 提供獨立的可加密式語音和視訊聊天，其開放標準稱之為 ZRTP. 要啟動這樣的加密聊天，你必須  
**第 1步.** 點擊 Jitsi 聯絡人清單上的某位聯絡人上的語音 (聯絡人名字下方左邊算來第2個) or 或視訊圖示(第3個) . 這將會彈出一個新視窗顯示Jitsi正在建立連線:![](http://self.jxtsai.info/%5C%22tool_jitsi22.png%5C%22)  
你的聯絡人將會看到一個來電通知  
**第2步.** 如果對方接受了這通來電你也會收到通知:![](http://self.jxtsai.info/%5C%22tool_jitsi23.png%5C%22)  
**注意** 那個紅色的小掛鎖圖示.它表示目前通話仍未採行ZRTP加密.  
**第3步.** 等候... Y你和對方的程式正在建立加密連線，這會花上一點時間. 如果成功了你將看到 _zrtp_字母顯示對應著橙色背景的關上掛鎖圖示，其如下圖所示.如果你無法成功建立連線 ,你仍可以通話但其並無加?密 .你可以試著離線重啟 Jitsi再試一次看看這次程式是否能順利加密連線 . 有時不同的聊天通訊服務提供者之間(如Google and Jit.si)ZRT加密功能無法運作.![](http://self.jxtsai.info/%5C%22tool_jitsi24.png%5C%22)  
**第4步.** 觀察_zrtp_ 字母下面部份掛鎖圖示會出現 一串字母與"伙伴比對"的訊息. 雙方查證確認是否看到的是相同的字母. 如果是的話,它表示你們之間的通訊已經受到加密保護了，其它人無法干擾.你可以點擊 **_「確認」Confirm_**. 而原本橙色的_zrtp_背景區也將轉變為綠色 :![](http://self.jxtsai.info/%5C%22tool_jitsi25.png%5C%22)  
**第5步.**現在你可以點擊黑色部份右上方的白色x標誌以關閉確認畫面:Jitsi 可讓你進行多方的語音和視訊通話.但注意在這種多方通訊情況下, ZRTP 加密得涉及多方之間啟動連線而不只是雙方彼此通話而已.

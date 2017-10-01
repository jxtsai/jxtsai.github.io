---
author: jx tsai
comments: true
date: 2016-06-15 09:01:00+00:00
layout: post
link: http://www.jxtsai.info/0928/2016/06/15/security-first-umbrella-app-%e4%b8%ad%e6%96%87%e5%8c%96%e6%bb%99%e6%95%b4/
slug: security-first-umbrella-app-%e4%b8%ad%e6%96%87%e5%8c%96%e6%bb%99%e6%95%b4
title: 'Security First: umbrella app 中文化滙整'
wordpress_id: 63
categories:
- human rights
- localization
- Security First
- umbrella app
---

![ SecurityFirst umbrella app](https://4.bp.blogspot.com/-gb5YwZLtFrQ/V34lVeJ1pjI/AAAAAAAAKTg/7iKBTomx3P88ewqB7f2lYO898E4JidBMwCLcB/s320/SecurityFirst-1024x490.png)  
之前提過會作一篇[Security First's umbrella app](https://secfirst.org/index.html) 滙整與中文化超連結整合，以讓未下載使用、觀看過原手機應用的讀者(其實指的就是錯亂的我自己本人)稍能有全盤的概念來想像這個手機應用程式（或更精準的說：一個手機上的隨身電子書）的內容。好了，本文就是那篇滙整。其原始碼與資料來源放在：　https://github.com/securityfirst/Umbrella_content/tree/master/html/en  
  
因為開發團體已把原始碼放在github上面，一開始還一度幻想自己可以先行私下製作一份本人專用的中文化手機版來試試。不過在這過程發覺因為字串長，另一語言版本（以中譯草稿為例）實在有許多細微又瑣碎的待校正補對之處，所以。。。。得再等上一段時間讓我來研究看看是否真有辦法自作中文版umbrella.apk。  
  
在下面的目錄架構中，也一併把放在本部落格貼出草稿的長文作了超連結的整理。（當然最終定版，還是得再靠其它有心人投入協助校正確認的工作，這樣正式的中文版不知何年何月才能被華文使用者看到啊Orz）.其它我所作的中文化初稿可在[transifex](https://www.transifex.com/otf/umbrella-app/)上找到，不過因為內容有點零碎，我日後再把它轉貼過來後一併會在本文中作連結的更新好了。  
  
umbrella app 目錄架構  


communications_email_advancedcommunications_email_beginnercommunications_making_a_call_beginnercommunications_mobile_phones_beginnercommunications_mobile_phones_expertcommunications_radios_and_satellite_phones_advancedcommunications_radios_and_satellite_phones_beginnercommunications_sending_a_message_beginnercommunications_social_media_beginnercommunications_the_internet_advancedcommunications_the_internet_beginneremergency_support_digital_beginneremergency_support_psyhical_beginnerinformation_backing_up_advancedinformation_malware_advancedinformation_malware_beginnerinformation_managing_information_beginnerinformation_passwords_advancedinformation_passwords_beginnerinformation_passwords_expertinformation_protecting_files_advancedinformation_safely_deleting_beginneroperations_arrests_beginneroperations_counter-surveillance_advancedoperations_counter-surveillance_beginneroperations_counter-surveillance_expertoperations_evacuation_beginneroperations_meetings_beginneroperations_protests_advancedoperations_protests_beginnerpersonal_protective_equipment_advancedpersonal_protective_equipment_beginnerpersonal_stress_advancedpersonal_stress_beginnerpersonal_stress_expertstrings[tools_adium:ADIUM 工具指南](http://self.jxtsai.info/2016/05/adium.html)[tools_android:安卓手機Android的基本安全設定指南](http://self.jxtsai.info/2016/05/android.html)[tools_chatsecure:ChatSecure工具指南](http://self.jxtsai.info/2016/05/chatsecure.html)[tools_cobian_backup:COBIAN 備份工具指南](http://self.jxtsai.info/2016/05/cobian.html)(X)tools_facebook（暫無中譯）[tools_jitsi:JITSI 工具指南](http://self.jxtsai.info/2016/05/jitsi.html)tools_k9_&_apg：　[K9 & APG工具指南](http://self.jxtsai.info/2016/06/k9-apg.html)[tools_keepassx:KEEPASS X 工具指南](http://self.jxtsai.info/2016/06/keepass-x.html)[tools_obscuracam:OBSCURACAM 工具指南](http://self.jxtsai.info/2016/06/obscuracam.html)[tools_orbot_/_orweb:ORBOT / ORWEB工具指南](http://self.jxtsai.info/2016/05/orbot-orweb.html)[tools_pgp_for_linux: PGP FOR LINUX 工具指南](http://self.jxtsai.info/2016/06/pgp-for-linux.html)（Ｘ）tools_pgp_for_mac_os_x（暫無中譯）（Ｘ）tools_pgp_for_windows（暫無中譯）[tools_pidgin:PIDGIN 工具指南](http://self.jxtsai.info/2016/05/pidgin.html)[tools_psiphon:PSIPHON 工具指南](http://self.jxtsai.info/2016/05/psiphon.html)[tools_recuva:RECUVA 工具指南](http://self.jxtsai.info/2016/06/recuva.html)[tools_redphone:REDPHONE 工具指南](http://self.jxtsai.info/2016/05/redphone.html)[tools_signal:SIGNAL 工具指南](http://self.jxtsai.info/2016/05/signal.html)[tools_textsecure:TextSecure 工具指南](http://self.jxtsai.info/2016/05/textsecure.html)[tools_tor_for_mac_os_x:TOR瀏覧器工具指南](http://self.jxtsai.info/2016/05/tor.html)(與下一篇整合為一篇)[tools_tor_for_windows:TOR瀏覧器工具指南](http://self.jxtsai.info/2016/05/tor.html)(與上一篇整合為一篇)travel_borders_beginnertravel_checkpoints_beginnertravel_kidnapping_advancedtravel_kidnapping_beginnertravel_kidnapping_experttravel_preparation_beginnertravel_vehicles_beginner  
  
重新再掃讀過幾遍umbrella app的內容大綱，其實也幫助我從個別的、技術性的泥洮跳開，有機會再重新思考更大的圖片，去理解為什麼有些社團組織亟力地呼籲民眾對於監控能力不斷擴張與公民權利之間互相拔河拉扯的角力。這些抵抗不只是科技上的道長與魔獸、大衛與巨人之間的對抗，其實更是原則與論述說理之間的對話。尤其在這兩天仔細讀了這篇：[Targeted surveillance, overpolicing and technology for resistance](http://beatricemartini.it/blog/targeted-surveillance-overpolicing-technology-for-resistance/)以及其上所整理提供的重要連結文件。  
  
如同umbrella app應用軟體在設計與資料取材過程中感謝的團體，關心此議題的朋友不妨多上他們的網站、訂閱電子報以及推特：  


  * Amnesty International
  * Ashoka Foundation
  * CARE International
  * Centre for Safety and Development
  * Committee to Project Journalists
  * Dart Center for Journalism and Trauma
  * Electronic Frontier Foundation：[Surveillance Self-Defense](https://ssd.eff.org/)(當無中文版，但ＥＦＦ一定要推的) 
  * European Commission's Humanitarian Aid and Civil Protection Department
  * European Interagency Security Forum
  * Frontline Defenders
  * Humanitarian Response
  * iiLab
  * Internews
  * LevelUp
  * Open Technology Fund
  * Overseas Development Institute
  * Protection International
  * Rory Peck Trust
  * Small World News
  * Tactical Technology Collective：[security in-a-box](https://securityinabox.org/zh/)（簡體中文版，也是大推）
  * The Engine Room
  * The Guardian Project
  * Videre

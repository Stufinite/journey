# journey

> 因為最近看了 `因為自動飲料機而延畢的那一年`  
所以就覺得 其實也該把這段時間的過程紀錄下來  
這之中的討論，構想等等  用日記的方式做紀錄  
也方便日後回來檢討

希望這不會是一段沒有結果的冒險 ㄎㄎ  
2017/01/31 大年初四

# 大架構

以天主教的`七原罪`來區分七大功能

1. 怠惰：課程類功能
 * 專案：[選課小幫手&行事曆(cal)](http://github.com/stufinite/cal)、[課程心得(feedback)](https://github.com/Stufinite/feedback_django)、[tiagenda](https://github.com/Stufinite/tiagenda)、[cphelper(選課查詢api)](https://github.com/Stufinite/cphelper)、[curso(課程搜尋引擎) ](https://github.com/Stufinite/curso)
 * 核心價值：一開始就只是覺得學校選課也太麻煩了吧  
   要拿一張紙抄抄寫寫的  所以我們要謹記  
   這個功能是滿足學生的`怠惰`  
   往後我們在新增功能時，如果發生爭執  或是收到負評（像是辦帳號）
   記得要依照核心價值 `怠惰` 去設計我們的服務
2. 暴食：今天吃什麼
  * 專案：[inferno（論壇框架+訂餐網頁版）](https://github.com/Stufinite/inferno)、[gluttony(訂餐api)](https://github.com/Stufinite/gluttony)、[time2eat-Android版](https://github.com/Stufinite/Time2eat-Android)、[time2eat印表機模組](https://github.com/Stufinite/Time2eat-printer)
  * 核心價值：學生吃飯的痛苦有兩點

      1. 每天都在苦惱要吃什麼  
      2. 尖峰時段用餐要等很久
    那我們要提供的服務就是有準確的`推荐系統`  
    以及快速的`手機定餐`、`第3方支付`的用餐體驗
  * 延伸：可以參考Gomaji結合餐飲  
    推荐特色旅遊
3. 色欲：交友網站
  * 核心價值：大學生參加團康、社團、系學會等等社交活動  
    都是想要接觸`女生`  這點一定要抓住  
    自介寫什麼很好聊、喜歡多交朋友的都是呷屎  
    都是想要認識妹子的  
    所以平台的介面、體驗一定要讓女生喜歡  
    沒女生就什麼都沒有了
4. 嫉妒：遊戲（暫定）
  * 核心價值：加速世界中的男主角因為經常被霸凌，所以沉迷於遊戲中強大的自己。希望我們的作品可以讓玩家`嫉妒`和羨慕在遊戲中的冒險與經歷。
  * 構想：想弄個類似`5年5百億`的作品，最好把七原罪每個函式庫和小幫手都擬人化，然後丟進遊戲當npc，這樣就可以讓遊戲跟我們的服務產生更多連結與話題性。賣座的話甚至可以賣周邊。
5. 傲慢：企業徵才（暫定）
  * 核心價值：
6. 貪心：校園購物網站（暫定）、打工平台，可以媒合簽約的店家和學生
  * 核心價值：
7. 憤怒：校園論壇（暫定）
  * 核心價值：
  * 像PTT一樣的文字版囉

架構圖如下：

![Alt text](http://g.gravizo.com/g?
 digraph G {
   sloth-> cal;
   sloth-> tiagenda;
   sloth-> feedback;
   sloth-> cphelper;
   sloth-> curso;
   gluttony -> inferno;
   gluttony -> gluttonyTw;
   gluttony -> "time2eat-Android";
   gluttony -> "time2eat-printer";
   lust -> "Dating site";
   envy -> Game;
   pride -> intern  ;
   wrath -> forum;
 })

# 爬蟲集合

與全部共用：[ptt爬蟲](https://github.com/Stufinite/ptt-web-crawler)

1. 怠惰：爬學校課程資訊、課程心得
 * 專案：[scrawler(課程爬蟲)](https://github.com/Stufinite/scrawler)
2. 暴食：爬餐廳資訊、鄉民的用餐心得
  * 專案：[time2eat爬蟲](https://github.com/Stufinite/Time2eat-crawler)
3. 色欲：
4. 嫉妒：
7. 傲慢：
  * 核心價值：
5. 貪心：
  * 核心價值：
6. 憤怒：

架構圖如下：

![Alt text](http://g.gravizo.com/g?
digraph G {
 sloth-> scrawler;
 sloth -> "ptt-web-crawler";
 gluttony -> "time2eat-crawler";
 gluttony -> "ptt-web-crawler";
}
)

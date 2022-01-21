```
01 Python 程式設計入門  
1-1 Python 變數、資料型別與運算子  
1-2 流程控制  
1-3 函式、模組與套件  
1-4 容器型別  
1-5 類別與物件  
1-6 檔案處理  
02 爬取的資料來源：HTML、CSV 和 JSON
2-1 HTML 與 CSS 基礎
2-2 資料標籤 – 文字和圖片標籤
2-3 群組標籤 – 清單、表格和結構標籤
2-4 網站巡覽 – 超連結標籤
2-5 互動介面 – 表單標籤
2-6 CSV 與 JSON
03 作業步驟一：認識網路爬蟲與 HTML 網頁分析
3-1 網路爬蟲與 URL 網址
3-2 認識 JavaScript 動態網頁內容
3-3 建立 Python 網路爬蟲的 SOP
3-4 使用開發人員工具分析 HTML 網頁結構
3-5 生活應用：分析 BBC News 新聞清單的標籤結構
04 作業步驟二：Requests 和 Selenium 取得網路資料
4-1 使用 requests 取得網路資料
4-2 使用 Selenium 取得網路資料
4-3 取得 HTML 表單送回的網路資料
4-4 使用 Web API 取得網路資料
4-5 生活應用：取得無限捲動分頁的網路資料
4-6 生活應用：剖析摩根台股指數的 JSON 資料
05 作業步驟三：BeautifulSoup 剖析和擷取網頁資料
5-1 使用 BeautifulSoup 擷取網頁資料
5-2 使用正規表達式擷取網頁資料
5-3 Selenium+BeautifulSoup 擷取網頁資料
5-4 如何破解網站的防爬機制
5-5 生活應用：爬取 BBC News 新聞清單
5-6 生活應用：Selenium 自動登入 Facebook
06 作業步驟四：Pandas 資料清理、讀取與儲存
6-1 Pandas 基本使用
6-2 Pandas 資料讀取與儲存
6-3 Pandas 常用的資料處理
6-4 Pandas 資料清理
6-5 生活應用：使用 Pandas 繪製視覺化圖表
07 應用實務：爬取食衣住行和娛樂資訊
7-1 擷取單一網頁的單一資料
7-2 擷取單一網頁的單筆記錄
7-3 擷取單一網頁的多筆記錄
7-4 擷取多頁網頁的多筆記錄
7-5 生活應用：爬取台鐵列車時刻 / 車次查詢資料
08 應用實務：爬取排行榜和網路趨勢資訊
8-1 爬取網站的排行榜資訊
8-2 認識 Google Trends 網路趨勢
8-3 pytrends 套件爬取 Google Trends 網路趨勢
8-4 生活應用：視覺化分析新冠肺炎的網路趨勢
09 整合應用：IFTTT、LINE 和 Telegram 發送通知訊息
9-1 註冊與使用 IFTTT 服務
9-2 申請與使用 LINE Notify
9-3 設定與使用 Telegram Bot 機器人
9-4 整合應用：IFTTT 和 LINE/Telegram 發送即時天氣訊息
10 應用實務：爬取 YouTube 等影音網站
10-1 爬取 YouTube 影片搜尋頁面
10-2 使用 pytube3 套件下載 YouTube 影片
10-3 下載 YouTube 聲音檔與字幕
10-4 生活應用：批次下載 YouTube 播放清單的影片
10-5 生活應用：爬取無限捲動分頁 YouTube 影片資料
10-6 生活應用：使用 You-Get 下載影音網站的影片
11 應用實務：爬取 Imgur 和 PTT 表特版圖片
11-1 爬取與下載網頁圖片
11-2 爬取 Imgur 網路相簿網站
11-3 爬取 PTT BBS 文章和表特版圖片
11-4 生活應用：使用 Python 批次下載爬取圖片
11-5 生活應用：爬取和下載 Instagram 圖片
12 整合應用：自動排程通知、爬取 / 下載資料和 Telegram Bot
12-1 使用 APScheduler 套件建立自動排程
12-2 建立 Telegram Bot 機器人
12-3 整合應用：自動排程送出通知訊息
12-4 整合應用：自動排程下載多媒體資料
12-5 整合應用：Telegram Bot 管家機器人
13 應用實務：爬取金融與商務資料
13-1 爬取即時匯率和匯率的歷史資料
13-2 使用 twder 套件爬取新台幣匯率
13-3 爬取上市櫃公司的金融數據
13-4 生活應用：爬取台灣證交所的券商資料
13-5 生活應用：使用上市公司月營收選出好股票
14 應用實務：爬取股市指數和股價數據
14-1 爬取股價指數和股價資料
14-2 使用 twstock 套件爬取台股股價
14-3 爬取 yahoo! finance 股價資料
14-4 爬取台股三大法人買賣超日報表
14-5 生活應用：繪製台積電股價的移動平均線
14-6 生活應用：使用 twstock 套件分析股票買賣點
15 整合應用：SQLite 資料庫和 Plotly 繪製互動圖表
15-1 SQLite 資料庫的基本使用
15-2 使用 Plotly 套件繪製網頁互動圖表
15-3 整合應用：將爬取的股票資料存入資料庫
15-4 整合應用：Plotly 繪製台積電股票的 OHLC 圖表
16 整合應用：Web API 和 LINE/Telegram Bot 聊天機器人
16-1 Flask 的基本使用
16-2 使用 Ngrok 取得外部 URL 網址
16-3 整合應用：Flask 建立 Web API
16-4 整合應用：Flask 建立 LINE Bot 聊天機器人
16-5 整合應用：Flask 建立 Telegram Bot 聊天機器人
A 安裝與使用Python 開發環境 - Anaconda 和 WinPython
（電子書，所有本書內文所提到的附錄A，請上博碩官網下載）
A-1 Anaconda 整合散發套件
A-2 WinPython 整合散發套件
A-3 Spyder 整合開發環境的使用
A-4 Python IDLE 整合開發環境的使用
A-5 使用pip 安裝 Python 套件
```

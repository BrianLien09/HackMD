
# JavaWeb入門
[TOC]
## 01. html快速入門

### html (超文本標記語言)
- 超文本:除了普通文字，像是超連結、音頻、圖片等等
- 標記語言: 由標籤"<標簽名>"構成語言
- - 標籤是預先定義好的，像是`<h1>`展示標題、`<img>`展示圖片等等
    HTML直接在瀏覽器運行，代碼由瀏覽器進行解析

#### 範例
##### 由==開始標籤==+==結束標籤==將==內容==包夾其中

```html
<h1>HTML入門</h1>
```
ps: 結束標前前面要記得加 `/`

##### 由單標籤構成

src為==屬姓名== ; src=後面為==屬性質==

```html
<img src="ing/1.pmg">
```
ps: 屬性質必須**用雙引號 or 單引號 包起來**

### CSS (層疊樣式表)

#### 範例
將標題變成==紅色==

```html
<h1 style="color:red;">HTML入門</h1>
```

[html標籤用法查詢](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a)

### html快速入門

1. 新建文本文件，後墜名為` .html`
2. 編寫HTML 的基本骨架，定義標題`<title>`(在瀏覽器上方顯示)

* * `<head>` 頭部標籤: 用來存放給瀏覽器的訊息，像CSS樣式
* * `<body>` 網頁主體: 用來存放給用戶看的訊息，如文字、圖片、影片
3. 在 `<body>` 中填寫內容

#### html基本骨架

```html
<html>
    <head>
        <title>HTML入門</title>
    </head>
    <body>
        <h1>Hello HTML</h1>
        <img src="ing/1.pmg">
    </body>
</html>
```
展示結果
![image](https://hackmd.io/_uploads/ry0GUwI8Je.png)

### html總結特點

* html標籤不區分大小寫，==建議小寫==
* html標籤屬性值使用單引號/==雙引號==都可以
* html語法結構不嚴謹，但==建議規範書寫==

## 02. VScode-html

### VScode 插建安裝

- HTML CSS Support
- JavaScript (ES6) code snippets
- Mithril Emmet
- Path Intellisense
- Vue 3 Snippets
- Auto Close Tag
- Auto Rename Tag
- open in browser
- Live Server
- Vue - Official
- File Utils
- IntelliJ IDEA Keybindings
- MarsCode AI: Coding Assi ...
- TONGYI Lingma

### setting.json
```json
{
    "workbench.colorTheme": "Default Light+",
    "code-runner.runInTerminal": true,
    "workbench.statusBar.visible": false,
    "editor fontramily": "'Courier New', Consolas, monospace" ,
    "editor.fontsize": 15,
    "editor.lineHeight": 1.8,
    "editor.tabsize": 2,
    "editor.codeActionsOnsave": {
        "source.fixAll": "explicit"
    },
    "editor.minimap.enabled": true,
    "liveServer.settings.donotshowInfollsg": true,
    "git.confirmsync": false,
    "terminal.integrated.defaultprofile.windows": "Command Prompt"
}
```
### VScode對於html之用法

* 輸入`!` 回車之後會出現==html基本架構==
* * 生成的結構標籤
```html
<!-- 聲明文檔類型為html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- 字符集 -->
    <meta charset="UTF-8">
    <!-- 設置網頁在移動設備上的顯示寬度以及縮放比例 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
* 輸入`ctrl + /` ==進行註釋==
* 只要==輸入標籤名即可==，回車之後將==自動補全==開始標籤以及結束標籤
```html
    <!-- 輸入 h1 回車之後，會自動生成一個一級標題 -->
    <h1></h1>
```
* 將指令輸入之後並==註釋==，最後回車，按下`tab` AI將完成你的指令
```html
    <!-- 定義一個一級標題，標題內容為Hello HTML -->
    <h1>Hello HTML</h1>
    <!-- 定義一個圖片，圖片來源為img/1.png -->
    <img src="img/1.png">
```

### 課程代碼紀錄
```html
<!-- 聲明文檔類型為html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- 字符集 -->
    <meta charset="UTF-8">
    <!-- 設置網頁在移動設備上的顯示寬度以及縮放比例 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML快速入門</title>
</head>
<body>
    <h1>HTML快速入門</h1>
    <img src="img/1.png">

    <!-- 定義一個一級標題，標題內容為Hello HTML -->
    <h1>Hello HTML</h1>
    <!-- 定義一個圖片，圖片來源為img/1.png -->
    <img src="img/1.png">
    <!-- 輸入 h1 回車之後，會自動生成一個一級標題 -->
    <h1></h1> 
</body>
</html>
```

## 03. 新聞標題實作-常見html標籤和CSS樣式

### 製作網頁新聞
#### 新聞-標題製作
**前言**
* html檔在瀏覽器渲染展示時，是==由上到下逐行解析==
* 故，編寫代碼時，==根據頁面佈局，從上往下寫==

**排版**
目標排版
![image](https://hackmd.io/_uploads/S1G8a_8I1x.png)


1.製作標題
關於標題標籤
![image](https://hackmd.io/_uploads/r1D00_UUye.png)
```html
<h1>美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影</h1>
```

2.製作標題下方左側超連結
```html
    <!-- 定義一個超連結，裡面展示 中央社 -->
     <!-- a 超連結標籤:
            href: 鏈結地址 - url地址
            target: 打開方式
                _black: 新頁面打開
                _self: 當前頁面打開(默認)
     -->
    <a href="https://www.cna.com.tw/" target="_blank">中央社</a>
```

3.標示時間
ps: html代碼換行，網頁並不會換行
故 實現目標排版有兩種
* 1. 直接在超連結代碼後直接空格並加上時間
```html
    <a href="https://www.cna.com.tw/" target="_blank">中央社</a> 2025-01-04
```
* 2. 超連結代碼換行後 再加上時間
```html
    <a href="https://www.cna.com.tw/" target="_blank">中央社</a>
    2025-01-04
```

### 小結

* 標題標籤: `<h1> - <h6>`
* 超連結標籤: `<a href="" target="">...</a>`
* * href: 指定資源訪問url
* * target: 指定在何處打開資源鏈接
    * * _self: 默認值，在當前頁面打開
    * * _blank: 在空白頁面打開
    
### 課程代碼紀錄

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影</title>
</head>
<body>
    <!-- 定義一個一級標題，標題內容為: 美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影 -->
    <h1>美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影</h1>

    <!-- 定義一個超連結，裡面展示 中央社 -->
     <!-- a 超連結標籤:
            href: 鏈結地址 - url地址
            target: 打開方式
                _black: 新頁面打開
                _self: 當前頁面打開(默認)
     -->
    <a href="https://www.cna.com.tw/" target="_blank">中央社</a>
    2025-01-04
</body>
</html>
```

## 04. 新聞標題實作 - CSS
### CSS 引入方式
* 行內樣式: 寫在標籤的style屬性中 (配合Javascript使用)

```html
<span style="color: gray;">2025-01-04</span>
```
* 內部樣式: 寫在style標籤中 (可以寫在頁面任何位置，但通常約定寫在head標籤中)

```html
<style>
    span {
      color: gray;
    }
</style>
```

* 外部樣式: 寫在一個單獨的.css文件中(需要通過link標籤在網頁中引入)

```css
span {
  color: gray;
}
```

引入link
```html
<link rel="stylesheet" href="css/news.css"
```

### 顏色表示形式
![image](https://hackmd.io/_uploads/rknAjYUL1e.png)

利用==拾色器== 找出目標樣式的顏色

### 小結
1. css引入方式
* * 行內樣式: `<h1 style="...">`
    內部樣式: `<style>...</style>`
    外部樣式: xxx.css  `<link href="...">`
    
3. 顏色表示
* * 關鍵字：red、gray
* * rgb表示法: rgb(255,0,0)
* * rgba: rgba(255,0,0,0.5)
* * 16進制: #ff0000、#cccccc、#f00
    
4. 顏色屬性
* * color: 設置文本內容的顏色

### 課程代碼紀錄
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影</title>
    <!-- 方式二: 內部樣式 -->
    <style>
        span {
            /* 關鍵字 */
            /* color: gray; */

            /* rgb表示法 */
            /* color: rgb(255, 0, 0) */

            /* rgba表示法 */
            /* color: rgba(255, 0, 0, 0.5)  */

            /* 16進制表示法 */
            /* color: #0000ff; */
            color: #7e7e7e;
        }
    </style>

    <!-- 方式三: 外部樣式 -->
    <!-- <link rel="stylesheet" href="css/news.css"> -->
</head>

<body>
    <!-- 定義一個一級標題，標題內容為: 美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影 -->
    <h1>美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影</h1>
    
    <!-- 定義一個超連結，裡面展示 中央社 -->
    <a href="https://www.cna.com.tw/" target="_blank">中央社</a>

    <!-- 方式一: 行內樣式 -->
    <!-- <span style="color: gray;">2025-01-04</span> -->
    <span>2025-01-04</span>

</body>
</html>
```

## 05. 新聞標題實作 - css選擇器

### CSS選擇器


| 選擇器 | 語法 | 示例 | 說明 |
|---|---|---|---|
| 元素選擇器 | 元素名稱 { ... } | h1 { ... } | 選擇頁面上所有 `<h1>` 標籤 |
| 類別選擇器 | .class屬性名稱 { ... } | .cls { ... } | 選擇頁面上所有 class 屬性為 cls 的標籤 |
| ID選擇器 | #id屬性名稱 { ... } | #hid { ... } | 選擇頁面上 ID 屬性為 hid 的標籤 |

### 去除超連結
```css
a {
            /* 去除超連結下劃線 */
            text-decoration: none;
        }
```

### 小結
* 元素選擇器: 標簽名 {...}
* 類選擇器: .class屬性值 {...}
* id選擇器: #id屬性值 {...}

* **優先級: id選擇器 --> 類選擇器 --> 元素選擇器**

### 課程代碼紀錄
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影</title>
    <style>
        /* 元素選擇器 */
        /* span {
            color: #7e7e7e;
        } */

        /* 類別選擇器 */
        /* .cls {
            color: #f00;
        } */

        /* id選擇器 */
        #time {
            color: #b2b2b2;
        }

        a {
            /* 去除超連結下劃線 */
            text-decoration: none;
        }
    </style>

</head>

<body>
    <!-- 定義一個一級標題，標題內容為: 美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影 -->
    <h1>美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影</h1>
    
    <!-- 定義一個超連結，裡面展示 中央社 -->
    <a href="https://www.cna.com.tw/" target="_blank">中央社</a>

    <span class="cls" id="time">2025-01-04</span>

</body>
</html>
```

## 新聞正文排版-引入圖片影片、段落

### 小結

| 標籤 | 作用 | 屬性/說明 |
|---|---|---|
| `<video>` | 視頻標籤 | src: 指定視頻的url (絕對路徑/相對路徑)<br>controls: 是否顯示播放控件<br>width: 寬度 (像素/相對於父元素百分比)<br>height: 高度 (像素/相對於父元素百分比) |
| `<img>` | 圖片標籤 | src, width, height |
| `<p>` | 段落標籤 |  |

### 資源路徑寫法

  * **絕對路徑**
      * 絕對磁碟路徑 (D:/xxx.jpg)
      * 絕對網路路徑 ([https://xxx.jpg](https://xxx.jpg))
  * **相對路徑**
      * 當前目錄: ./ (可以省略)
      * 上一級目錄: ../

### 課程代碼紀錄
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影</title>
    <style>
        /* id選擇器 */
        #time {
            color: #b2b2b2;
        }

        a {
            /* 去除超連結下劃線 */
            text-decoration: none;
        }
    </style>

</head>

<body>


    <!-- ----------------------------------新聞標題 ------------------------------------------>
    <!-- 定義一個一級標題，標題內容為: 美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影 -->
    <h1>美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影</h1>
    
    <!-- 定義一個超連結，裡面展示 中央社 -->
    <a href="https://www.cna.com.tw/" target="_blank">中央社</a>

    <span class="cls" id="time">2025-01-04 15:51</span>

    <br><br>
    <!-- ----------------------------------新聞正文 ------------------------------------------>
    <!-- 定義一個影片，引入 video/news.mp4 -->
    <!-- video標籤屬性
        src: 影片來源
        controls: 顯示播放控鍵
        autoplay: 自動播放
        width: 寬度(建議: 寬度和高度只要設置一個就好，另一個會等比例縮放)
        height: 高度
          單位:
            px: 像素
            %: 百分比 (相對於父元素的百分比)  
    -->
    <!-- <video src="video/news.mp4" controls width="80%"></video> -->
    <!-- <audio src="audio/news.mp3" controls></audio> -->

    <!-- 定義一張圖片，引入 img/news.gif -->
    <!-- img標籤屬性
            src: 圖片訪問地址
                1. 絕對路徑: 
                    1.1 絕對磁盤路徑: D:\Brian\HTML-CSS\img\news.gif (不推薦)
                    1.2 絕對網路路徑: http://www.baidu.com/img/news.gif
                2. 相對路徑: img/news.gif
                    2.1 ./ : 當前目錄 (可以省略), 例如: ./img/news.gif => img/news.gif
                    2.2 ../ : 上一級目錄
    -->
    <img src="img/photo.jpg" width="60%"></img>
    
    <p>
        美國消費性電子展（CES）本月7日將在拉斯維加斯登場，具人工智慧（AI）的裝置、機器人和車輛將爭相吸引目光，供應商們則將設法因應美國總統當選人川普揚言加徵的關稅。
    </p>

    <p>
        AI將在這次消費性電子展成為一大焦點，另外像是拖拉機、船隻、割草機和高爾夫球袋推車等自動化機具也將引發關注。各大廠商將在這場年度盛會正式開幕前數天搶先舉辦新品發表活動。
    </p>
    
    <p>
        美國科技業諮詢公司「創意策略」（Creative Strategies）分析師米拉奈西（Carolina Milanesi）告訴法新社：「所有人的話題都將圍繞AI…從冰箱到烤箱到其他產品，無論是否真的有AI，所有人都會設法和AI沾上邊。」
    </p>

    <p>
        美國獨立科技業趨勢分析師恩德勒（Rob Enderle）指出，AI晶片巨頭輝達（NVIDIA）執行長黃仁勳將在CES開幕前夕發表一場「非聽不可」的主題演講，展示輝達的創新成果。
    </p>

    <p>
        此外，消費性電子展也將成為一場大型汽車展，車商和零件供應商將展示自動駕駛與自動化安全功能。
    </p>

    <p>
        研究公司Techsponential分析師格林加特（Avi Greengart）說：「CES早已成為汽車展，如果真要說，今年更是如此。」
    </p>
    
    <p>
        恩德勒也認為，儘管飛行車要應用於日常還有很長的路要走，但仍會是這次CES一大看點，「應該會開始看到可以購買的飛行運輸工具…但取得飛行許可又是另一回事了」。
    </p>

    <p>
        川普屢次提及上任後將加徵關稅，恐提高進口產品成本。多名分析師都表示，在本次消費性電子展中，關稅議題很可能是鎖定美國市場的參展者關注焦點之一。
    </p>

    <p>
        恩德勒分析，許多展出產品都包含進口零組件，若川普真的對加拿大、中國和墨西哥加徵關稅，價格勢必將大幅上漲，這次展場「將有許多感到擔憂的廠商…但很多討論都將閉門舉行，以免激怒即將上任的政府」。
    </p>

    <p>
        格林加特認為，這些閉門討論將包括如何因應關稅可能導致的供應鏈限制。
    </p>
</body>
</html>
```

## 新聞正文樣式

### 字體加黑加粗-兩種
1. `<b>`
```html
<b>美國消費性電子展</b>
```
2. `<strong>`
```html
<strong>美國消費性電子展</strong>
```

### 首行縮進

1. `&nbsp;`
```html
<strong>&nbsp;&nbsp;&nbsp;&nbsp;美國消費性電子展</strong>
```
2. `text-indent`
```css
text-indent: 2em;  /* 首行縮進2個字符 */
```

### 小結

| 標籤 | 作用 | 屬性/說明 |
|---|---|---|
| `<b>` 或 `<strong>` | **加粗** | `<strong>` 具有語意化，表示強調內容 |
| `<u>` 或 `<ins>` | **下劃線** | `<ins>` 具有語意化，表示插入的內容 |
| `<i>` 或 `<em>` | **斜體** | `<em>` 具有語意化，表示強調的文字 |
| `<s>` 或 `<del>` | **刪除線** | `<del>` 具有語意化，表示刪除的內容 |

| 字元實體 | 作用 | 屬性/說明 |
|---|---|---|
| `&nbsp;` | **空格** | 不斷行的空格 |
| `&lt;` | **小於符號** | 用於表示 HTML 標籤的開始 |
| `&gt;` | **大於符號** | 用於表示 HTML 標籤的結束 |

#### CSS 屬性：

| 屬性 | 作用 | 說明 |
|---|---|---|
| `line-height` | **設定行高** | 控制行與行之間的距離 |
| `text-indent` | **設定行首縮排** | 控制段落第一行的縮排距離 |

### 課程代碼紀錄

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影</title>
    <style>
        /* id選擇器 */
        #time {
            color: #b2b2b2;
        }

        a {
            /* 去除超連結下劃線 */
            text-decoration: none;
        }

        p {
            /* 設置段落的行高 */
            line-height: 2;
            /* 設置首行縮進 */
            text-indent: 2em;  /* 首行縮進2個字符 */
        }
    </style>

</head>

<body>


    <!-- ----------------------------------新聞標題 ------------------------------------------>
    <!-- 定義一個一級標題，標題內容為: 美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影 -->
    <h1>美國消費性電子展聚焦AI科技 分析師：許多廠商籠罩川普關稅陰影</h1>
    
    <!-- 定義一個超連結，裡面展示 中央社 -->
    <a href="https://www.cna.com.tw/" target="_blank">中央社</a>

    <span class="cls" id="time">2025-01-04 15:51</span>

    <br><br>
    <!-- ----------------------------------新聞正文 ------------------------------------------>
 
    <img src="img/photo.jpg" width="60%"></img>
    
    <p>
        <!-- <b>美國消費性電子展</b> -->
        <!-- <strong>&nbsp;&nbsp;&nbsp;&nbsp;美國消費性電子展</strong> -->
        <strong>美國消費性電子展</strong>
        （CES）本月7日將在拉斯維加斯登場，具人工智慧（AI）的裝置、機器人和車輛將爭相吸引目光，供應商們則將設法因應美國總統當選人川普揚言加徵的關稅。
    </p>

    <p>
        AI將在這次消費性電子展成為一大焦點，另外像是拖拉機、船隻、割草機和高爾夫球袋推車等自動化機具也將引發關注。各大廠商將在這場年度盛會正式開幕前數天搶先舉辦新品發表活動。
    </p>
    
    <p>
        美國科技業諮詢公司「創意策略」（Creative Strategies）分析師米拉奈西（Carolina Milanesi）告訴法新社：「所有人的話題都將圍繞AI…從冰箱到烤箱到其他產品，無論是否真的有AI，所有人都會設法和AI沾上邊。」
    </p>

    <p>
        美國獨立科技業趨勢分析師恩德勒（Rob Enderle）指出，AI晶片巨頭輝達（NVIDIA）執行長黃仁勳將在CES開幕前夕發表一場「非聽不可」的主題演講，展示輝達的創新成果。
    </p>

    <p>
        此外，消費性電子展也將成為一場大型汽車展，車商和零件供應商將展示自動駕駛與自動化安全功能。
    </p>

    <p>
        研究公司Techsponential分析師格林加特（Avi Greengart）說：「CES早已成為汽車展，如果真要說，今年更是如此。」
    </p>
    
    <p>
        恩德勒也認為，儘管飛行車要應用於日常還有很長的路要走，但仍會是這次CES一大看點，「應該會開始看到可以購買的飛行運輸工具…但取得飛行許可又是另一回事了」。
    </p>

    <p>
        川普屢次提及上任後將加徵關稅，恐提高進口產品成本。多名分析師都表示，在本次消費性電子展中，關稅議題很可能是鎖定美國市場的參展者關注焦點之一。
    </p>

    <p>
        恩德勒分析，許多展出產品都包含進口零組件，若川普真的對加拿大、中國和墨西哥加徵關稅，價格勢必將大幅上漲，這次展場「將有許多感到擔憂的廠商…但很多討論都將閉門舉行，以免激怒即將上任的政府」。
    </p>

    <p>
        格林加特認為，這些閉門討論將包括如何因應關稅可能導致的供應鏈限制。
    </p>
</body>
</html>
```

## 新聞整體版面-css盒子模型


### 盒子模型

* **盒子：** 在網頁中，所有的元素（標籤）都可以看作是一個盒子。這個盒子將元素包含在一個矩形區域內，方便我們進行頁面布局。
* **盒子模型的組成：** 每個盒子都由四個部分組成：
  * **內容區（content）：** 存放元素的實際內容。
  * **內邊距區（padding）：** 內容區與邊框之間的區域。
  * **邊框區（border）：** 包圍內容區和內邊距區的邊框。
  * **外邊距區（margin）：** 邊框與其他盒子之間的區域。


### 盒子模型與佈局標籤

#### 布局標籤
* **網頁開發中，常用 `div` 和 `span` 這兩個沒有語義的佈局標籤。**

### 特點
* **`<div>` 標籤:**
  * 一行只顯示一個（獨占一行）
  * 寬度默認是父元素的寬度，高度默認由內容撐開
  * 可以設置寬高（`width`、`height`）
* **`<span>` 標籤:**
  * 一行可以顯示多個
  * 寬度和高度默認由內容撐開
  * 不可以設置寬高（`width`、`height`）

* **示例代碼：**
  ```css
  div {
      width: 200px;
      height: 100px;
      background-color: #95A5D2;
      padding: 20px 20px 20px 20px;
      border: 20px solid #6BD5D7;
      margin: 30px 30px 30px 30px;
  }
  ```
  * **`width`、`height`：** 設置盒子寬度和高度。
  * **`padding`：** 設置內邊距，分別代表上、右、下、左的內邊距。
  * **`border`：** 設置邊框，分別代表邊框寬度、樣式和顏色。
  * **`margin`：** 設置外邊距，分別代表上、右、下、左的外邊距。



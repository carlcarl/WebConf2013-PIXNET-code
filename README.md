# WebConf 2013 PIXNET 擺攤題目
http://webconf2013.events.pixnet.net/

## 1. JSON
這題算是 call API 的基本題，在 API 裡面查一下就可以查到格式(如下)，而且 call API也沒什麼限制：

	http://emma.pixnet.cc/blog/articles/61695293?user=emmademo

只要引用 jQuery 呼叫 getJSON，配合 JSON 的 parse 就能拿到文章的內容資料了。

## 2. Webfonts
送分題，只要有部落格，然後在部落格裡面加入 justfonts 網站提供的 script 就能秒殺了。

## 3. Offline Web App
花比較多時間的一題，因為之前沒寫過這種東西orz。這邊要先利用 Application Cache 將靜態資料作 cache，要 cache 哪些資料必須在 manifest.mf 這個檔案裡面設定，，另外還有很重要的一點要注意就是：要設定 Web Server 處理 mf 副檔名的格式，以 nginx 為例，要在 mime.types 檔案裡的 `types` 中加入以下內容:

	text/cache-manifest			mf manifest;
測試的話只要把網路關掉，再重新整理網頁，如果沒出現連線錯誤就表示成功了。再來是文章內容的部份，這部份跟第一題一樣，不過因為 Application Cache 只能 cache 靜態的資料，所以這邊呼叫 API 的部份要加上 Local Storage，如果 Local Storage 裡面有就用 Local Storage裡的，沒有的話再呼叫 API，呼叫完再把資料存到 Local Storage 裡。

## 4. Responsive Design
直接套 bootstrap (炸)，也可以自己土炮啦...，不過沒啥時間，所以乾脆套一套比較快XD，測試的話就用手機開看看，如果畫面縮成適合手機觀看的寬度就表示 OK 咧。

## 5. OpenID
因為後來沒啥時間，所以就沒寫這題了:P


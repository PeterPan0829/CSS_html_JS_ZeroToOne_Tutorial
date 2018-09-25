# 基本 html 架構

-----------------------------

html就像是一個人的的骨頭(骨架)，也可以是101大樓的鋼筋水凝，	
我們將 < > 框起來的東西叫做標籤會有起始標籤以及結束標籤` <html>` (起始標籤) `</html> `(結束標籤)

​	

今天就先來建一個擁有基本html架構的網站吧！

1. 建立index.html檔案 -> 新增檔案

`<!DOCTYPE html>`

 一定會在html檔案的的第一行，在`<html>`標籤前面，但他不是html標籤，它是瀏覽器要使用哪個版本的html進行編寫的指令

​	

`<html> </html>`

 包住整個網頁的重要標籤，有起始標籤也有結束的標籤

​	

`<head> </head>`

包在 html標籤裡，因為它都放在最上方所以叫 head 標籤之間，可以用來放很多網頁資訊，像是給瀏覽器看的或者是導入外部ＣＳＳ、ＪＳ檔案，最常見的不外乎就是`<link> <style> <script> <meta>`

​	

`<title> </title>`

是我們網站的名字，也就是你在標籤頁上看到的網站名稱

​	

`<body> </body>`

都直接叫身體了，就是我們網站想要顯示的內容都會放在body裡

​	

不免俗的來一下 Hello World!

在`<body></body> `直接打上 Hello World!

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
</head>

<body>
  Hello World!!!!!!!!!
</body>

</html>
```


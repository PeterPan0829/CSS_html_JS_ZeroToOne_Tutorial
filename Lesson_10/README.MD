# 版型設計切版(二)＿基本框架_3

圖片呢？？？？？？？？？？img/29_版型設計07（請記得換成自己的）.jpg

左邊的區塊分為兩個區塊：
1. 上方：banner區塊，在banner區裡面再包一個我們網站大標的區塊
2. 下方：最新文章區塊



## banner區塊
先看左側選單的部分被我分成三塊
```html
<div class="content">
    <div class="banner">
        <div class="picture"></div><!--放置圖大頭照的div區塊-->
        <span>Peter<br>#人生剩力組<br>Software Developer at StartUp</span>
    </div>
</div>
```

新增一個`div`在`content`裡面，給它一個`class="banner"` 再來是樣式

```css
.content .banner {
     width: 100%;/*設定寬度為100%*/
     height: 300px;/*設定高度為300px*/
     background-color: rgb(44, 154, 218);
 }
```


> **寬度**基本上都是使用**百分比%**或是**vw**。
>
> 原因是為了避免在改變視窗大小的時候發生**破版（跑版）**。

​	

### 結果

![36](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/36_%E7%89%88%E5%9E%8B%E8%A8%AD%E8%A8%8814.jpg)

​	


### 最新文章區
一樣新增一個`div`包在`content`裡面，
那新增文章的部分是一個類似清單的東西所以我們這邊用`<ul>`、 `<li>` 來做，
下面 **more** 的部分則是要連回指定的網址所以我們使用 **a**。

```html
    <div class="content">
    <div class="banner">
      <div class="picture"></div>
      <!--放置圖大頭照的div區塊-->
      <span>Peter
        <br>#人生剩力組
        <br>Software Developer at StartUp
      </span>
    </div>
    <!-- ＝＝＝＝＝＝＝＝＝＝看這裡＝＝＝＝＝＝＝＝＝＝ -->
    <div class="news">
      <div>最新文章</div>
      <ul>
        <li>蘋果日報</li>
        <li>不自由日報</li>
        <li>二周刊</li>
      </ul>
      <a href="#">More</a>
    </div>
    <!-- ＝＝＝＝＝＝＝＝＝＝看這裡＝＝＝＝＝＝＝＝＝＝ -->
  </div>
```

幫最新文章 **news** 加上 `style`

```css
.content .news {
  /*顯示news的區塊範圍*/
  background-color: rgb(29, 185, 113);
}
```

​	

### 結果

![37](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/37_%E7%89%88%E5%9E%8B%E8%A8%AD%E8%A8%8815.jpg)

到這邊可能會有個疑問，為什麼不是把整個區塊都站滿呢？	
因為不需要，`banner `只是看起來 **好像佔滿整個區塊**。但其實是因為給它高度去佔著那個區域，可是它也只是一個區塊放在裡面而已；而 **最新消息 NEWS** 的部分因為沒有這麼大張圖片要放，所以先沒有預設高度給它。	

接下來我們會逐一調整每個區塊跟元件的樣式跟位置，這些沒有在設計圖上出現的顏色之後都會拿掉，用意都是讓大家區分區塊而已。

那我們**主要的框架**部分就是這樣而已，不要想太難～～

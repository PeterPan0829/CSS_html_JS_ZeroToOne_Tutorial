# 版型設計切版(二)_基礎樣式1 _ 內距與外距

## 內距 padding ＆ 外距 margin
在排版很常用到的 **內距 padding ＆ 外距 margin**

首先從**title** 開始，先上個設計圖的樣式。

圖片呢？？？？？？？？？？img/29_版型設計07（請記得換成自己的）.jpg


在 **title** 裡的大頭照是圓形的，要利用 **CSS畫圓** 的話就是使用`border-radius`也就是**圓角**，如果沒給特別的屬性區塊都是四四方方的，所以加上圓角跟微調一下大小。

### 完整的大頭貼區塊 CSS
```css
.menu .title .min_picture {
     background: url('../img/imgTag_un.jpg') no-repeat;
     background-size: 100px auto;
     height: 100px;
     width: 100px;
     border-radius: 50px;  // 圓角
     display: inline-block;
 }
```

> border-top-left-radius - 設定左上角
> border-top-right-radius - 設定右上角
> border-bottom-right-radius - 設定右下角
> border-bottom-left-radius - 設定左下角

​	

### 結果

![38](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/38_%E7%89%88%E5%9E%8B%E8%A8%AD%E8%A8%8816.jpg)

​	

## 開發者工具再次派上用場！！！
假設有點太大或太小了，那怎麼辦？要一直來回設定數字好麻煩！	
這時候再次打開你的開法者工具並且選擇我們大頭貼的區塊。

![39](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/39_%E7%89%88%E5%9E%8B%E8%A8%AD%E8%A8%8817.jpg)

這時候就可以直接從這邊一邊調整一邊看結果了！

> 按上或下可以直接調整數字，按住`shift`在按上或下，一下為增加或減少10px

### 調整好的樣式
```css
.menu .title .min_picture {
  background-size: 95px auto;
  height: 95px;
  width: 95px;
 }
```

可是還有位置部分沒有調，這時候我們可以用兩種方式：**內距** 與 **邊距**

1. **內距 padding**：我們設定 **title** 與它的內容的距離
2. **外距 margin** : 設定**min_picture**他與他旁邊的元素的距離

-------------------------

## padding的做法

屬性說明：

> padding:40px ->上下左右邊與內容距離40px
>
> padding:40px 10px -> 目前距離上下邊與內容距離40px 距離左右邊與內容距離10px
>
> padding: 15px 10px 20px 5px -> 上邊與內容距離 15px,右邊與內容距離10px,下邊與內容距離20px,左邊與內容距離5px
>
> 那也可以這樣寫 padding-top 就是直接指定上內距，以此類推就有左邊、右邊、下面 left、right、bottom等 ...

**title** 目前是有設定高跟寬的，假設使用 **padding** 的話就必須把高跟寬拿掉，否則會變成這樣：

![40](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/40_%E7%89%88%E5%9E%8B%E8%A8%AD%E8%A8%8818.jpg)

​	

拿掉 **title** 高與寬，設定內距的完整樣式如下：

```css
.title {
     padding: 20px 15px;
     background-color: #4A4A4A;
 }
```

### 結果
![42](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/42_%E7%89%88%E5%9E%8B%E8%A8%AD%E8%A8%8820.jpg)

------------------------------------

## margin的做法

屬性說明：

> **margin:40px** ->距離上下左右邊 **40px**
>
> **margin:40px 10px ->** 目前距離上下邊 **40px** 距離左右邊 **10px**
>
> **margin: 15px 10px 20px 5px** -> 離上面 **15px**, 離右邊 **10px**, 離下面 **margin**,離左邊 **5px**
>
> 那也可以這樣寫 **margin-top** 就是直接指定距離上面多少，以此類推就有左邊、右邊、下面 left、right、bottom等 

-------------------------------------



## The philosophy

從 **屬性說明** 當中，有發現什麼嗎？	
設定屬性的方式 **padding: 15px 10px 20px 5px** 這就是順時針的概念！	
這樣記就好，別想太複雜～	

​	

而回到 margin 上就是由`.min_picture`的部分去調整	
**將title的寬與高加回去並拿掉padding**：

```css
.menu .title .min_picture {
  background: url('../img/imgTag_un.jpg') no-repeat;
  background-size: 95px auto;
  height: 95px;
  width: 95px;
  border-radius: 50px;
  display: inline-block;
  margin: 20px 15px;
}
```

### 結果
![43](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/43_%E7%89%88%E5%9E%8B%E8%A8%AD%E8%A8%8821.jpg)

這裡是寫 **距離上下 20**，**距離左右 15**。	
假如畫面有破版、跑版的問題，請回頭看一下，還記得我們將 title 的高度設定為 100px 嗎？	
參考個方式 - **加法**，首先是上下的邊距 **20px + 20px**，再來是我們圖邊的高度 **95px**，這樣是不是總共是 **135px**？目前沒有影響到文字的部分，因為現在寫的是單就這張圖片的邊距是沒超過的，可以自己動手玩玩看隨便設定數值看看跑版的情況唷～


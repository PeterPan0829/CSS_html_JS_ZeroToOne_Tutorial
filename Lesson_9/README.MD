# 版型設計切版(二)_基本框架_2 & 圖片的顯示方法

圖片呢？？？？？？？？？？img/29_版型設計07（請記得換成自己的）.jpg

慢慢開始把選單跟內容的部分都放進去，之後再開始寫細部的樣式


## 左側選單
先看左側選單的部分被我分成三塊

## 第一個區塊
第一個區塊的部分是我們網頁的title的部分，這裡分享兩種方式
很明顯這個區塊有一張圖片跟一串文字是使用 **img** 以及 **span**

> 為什麼不是用p或是h1之類的？

因為我個人習慣字體的大小基本上都會另外調過，
再加上我們有加 **resrt.css** 的關係，所以標題類的大小都變成一般大小了

**img標籤的用法**
```js
<img src="圖片位置" alt="圖片的描述文字">
```

圖片位置分別有 **絕對位置** 與 **相對位置**
* 絕對位置：就是完整個路徑，死的，假設換了一個資料夾就會整個壞掉（除非你使用的圖片是超連結的）
* 相對位置：就是相對於我們目前的檔案他在哪裡，建議使用任何圖片的時候盡量用相對位置
這邊所使用的圖片位置為相對位置，前面的點的位置為往前一個資料夾的意思，所以兩個點就是往前兩個資料夾


> VS Code 套件推薦(讓選擇檔案位置更方便)
[Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)

### html
```js
<!-- menu為我們的左側選單框架 -->
<div class="menu">
<!-- 因為這是一個小區塊所以我們也使用一個div來包裹裡面的東西，並且給他一個class樣式方便我們調整-->
  <div class="title">
      <img src="./img/imgTag.jpg" alt="大頭貼">
      <span>Peter</span>
  </div>
</div>
```

### 結果

圖片呢？？？？？？？？？？img/30_版型設計08.jpg

圖片顯示但太大張了，所以我們簡單的調整一下大小
先加上一個 class
```js
<img class="imgStyle" src="./img/imgTag_un.jpg" alt="大頭貼">
```

```js
/*這邊將他的層級關係也寫進去，他是在 menu > title底下*/
.menu .title .imgStyle {
     width: 50px;
 }
```

### 結果

圖片呢？？？？？？？？？？img/31_版型設計09.jpg

另一種方式是我們將圖片的部分使用 **css** 的 **background** 屬性

### html
```js
  <div class="menu">
    <div class="title">
      <!--給這個div一個class -> min_picture -->
      <div class="min_picture"></div>
      <span>Peter</span>
    </div>
  </div>
```

看 **html** 目前是沒有任何東西的，讓我們加上style

```js
.menu .title .min_picture {
     background: url('../img/imgTag_un.jpg') no-repeat;
     background-size: 50px auto;
     height: 50px;
     width: 50px;
     display: inline-block;
 }
 ```


**background**：url('圖片位置') **no-repeat** 代表這張圖片不重覆
**background-size**：兩個值分別為 高 寬 我們設定背景圖片大小為 高為50px 寬度自動
**height**：設定高度為50px
**width**：設定寬度為50px

**no-repeat** 也可以獨立設置成 **background-repeat:no-repeat;**
**這邊可以去試試看如果不加寬高的話會發生什麼事**

**display**：專門用來設定區塊屬性的屬性。
因為 **div本身就是一個區塊**，所以它會將文字的部分往下推，
但是我們要讓它們是 **並列的** 所以加上 **inline-block** 這個屬性給它


### 結果

圖片呢？？？？？？？？？？img/32_版型設計10.jpg

這兩種方式的差異有發現到嗎？我個人喜歡第二種方法。
因為只需要去更改 **main.css** 樣式那整個區塊都可以自由去改變，不管是要換哪張圖片還是圖片要移動顯示哪個位置都可以，
但如果使用 **img** 的話，只要改檔案圖片那就必須跟著改，而且必須將圖片的尺寸都設定好，才不會因為設定死的寬高讓它變形。

接下來把這一個區塊的樣子切出來，加入 **title** 這個 class 的樣式。

```js
 .title {
     /*這邊的寬度100%是抓menu設定的寬度*/
     width: 100%;
     /*寫一個適合的高度*/
     height: 100px;
     /*設定底色為#4A4A4A*/
     background-color: #4A4A4A;
 }
```

圖片呢？？？？？？？？？？img/33_版型設計11.jpg

## 第二個區塊

這個區塊就是主要選單的部分，
其實沒有很麻煩，因為節省難度所以設計直式單層的選單

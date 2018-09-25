# 版型設計切版(ㄧ)＿基本框架＿1

前面有簡單提過切版這件事，那今天我們就要來深入了解。

-----------------------------------



## 何謂切版？
我們將設計師已經設計好的 **Mockup 靜態的原稿** 製作成網頁

​	 

## 那怎麼切版？
我個人的話會先把設計圖先區塊化分好，以區塊內的元件標籤都分析好才會開始寫`html`的靜態架構
將[Lesson7](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/Lesson_7/README.MD)那張設計稿大致上切成以下圖片。

圖片呢？？？？？？？？？？img/25_版型設計03（請記得換成自己的）.jpg

​	

黑色框框是大框架最主要的部分，粉紅色框框則是裡面的小區塊、綠色框框則是我分析出來要使用`li`去製作的區塊
所以大大小小區塊初步分析起來大概是8塊～

那我們在這裡開始所有關於`css`的部分都是會以**引入的方式**做使用（模擬開發網頁的實際情形）

附上語法：

```html
<link rel="stylesheet" href="css位置">
```
主要是為了可讀性，所以我喜歡把檔案都分清楚，`css`檔裡面的寫法跟在`style`標籤裡的寫法一樣。

​	

## 開始

### 1.先建立專案資料夾、建立檔案

* 建立資料夾

  我自己的習慣，會在主要目錄底下再分成四個資料夾：**css**、**sass**、**js**、**img**。
  因為我們目前大概只會使用`css`以及`img`所以就只建立這兩個資料夾，之後所有的圖片都會整理到`img`這個資料夾，`css樣式`也都是整理到`css`這個資料夾。

* 建立index.html

  ![26](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/26_%E7%89%88%E5%9E%8B%E8%A8%AD%E8%A8%8804.jpg)

  ​	

* 在`css`資料夾內建立`main.css`
  這邊的`css`名稱並沒有限制說要取什麼，但結尾記得是`.css`檔名。

  ​	

* 在css資料夾內建立`reset.css`
  因為每個瀏覽器所預設的的`css`預設值都不太一樣，所以常常會為了要讓每個平台一樣根據瀏覽器去做各種不同樣式的調整，也就是所謂的**破版**(在chrome看正常，去了ie就壞掉了)


這裡大力推薦一支`css`會將**所有的預設值通通歸零**並適應在任何瀏覽器，讓你在切版的時候可以省比較多的功夫，就是 **reset**。它是`CSS`大師 Eric A. Meyer整理出的 [Reset CSS](https://meyerweb.com/eric/tools/css/reset/)。

​	

### 使用方法
1. [點我開啟下載頁面](https://meyerweb.com/eric/tools/css/reset/reset200802.css)
2. 將裡面的內容通通複製到我們剛剛開的 **reset.css**，或是直接另存網頁到我們 **css資料夾**

* 在 `main.css` 將 reset.css 引進來`@import './reset.css';`
  在 `main.css` 的最上頭將這一行加入就可以了

-------------------------

### 2.建立html架構
* 建立基本的html架構
[回顧建立html架構](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/tree/master/Lesson_2)

* 建立框架
我們使用 `div` 先建立兩個區塊並且給他`class`的名稱。
**左側選單 class="menu";**
**右側內容 class="content";**

```html
<div class="menu"></div>
<div class="content"></div>
```

* 在main.css新增樣式.menu 製作左側選單
  製作側邊選單的樣式，那在這裡先簡單分析他會需要有的屬性

1. 固定於左側浮動不變
2. 高度為整個畫面的高度

```css
 .menu {
     height: 100vh;
     width: 300px;
     background-color: #7C7C7C;
     float: left;
 }
```

**height**：使用比較新一點的新屬性`vh`，讓我們的左側選單的高度**可以跟著視窗高度做改變**。
**width**：選單的寬度設定為`300px`。
**background-color**：設定背景顏色。
**float**：將視窗浮動於左側。

### 結果

![27](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/27_%E7%89%88%E5%9E%8B%E8%A8%AD%E8%A8%8805.jpg)

​	

在`main.css`新增樣式 `.content`製作左側選單佔滿右側區塊

```js
.content {
  width: 100vw;
  height: 100vh;
  background-color: rgb(130, 202, 196);
}
```

**width**：`vh`是跟著視窗高度(height)，所以`vw`就是跟著視窗寬度(width)，讓我們右側的內容區塊能隨著視窗寬度做改變。
**height**：這邊為了配合之後的頁面所以也使用`vh`，那其實也可以不用設定這一個區域的高度。
**background-color**：為了讓大家看區塊所以加上背景色，我們版型設計底色是白色所以這個屬性會拿掉（這裡只是示範）。

​	

### 結果

![28](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/28_%E7%89%88%E5%9E%8B%E8%A8%AD%E8%A8%8806.jpg)

那我們主要的大框架就好了，之後我們就來把剩下的所有小區塊塞進去。

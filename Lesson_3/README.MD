# 常用標籤(二) _ div、span

----------------------------------

## 本次主題是在做網站**切版**時很常用到的標籤 - div、span

​	

### 什麼是切版呢？
簡單說，切版就是我們將設計師設計好的畫面製作成網頁我們會將畫面分類成一個一個的區塊，然後開始進行頁面的製作。

本次要分享的就是 div 以及 span。

​	

* div

簡單的說就是一個區塊，我們會在裡面塞很多很多東西。

假設人體是一個網頁，那每個器官和部位對於人體來說就是一個一個區塊，那每個器官裡面都有細胞和組織，這些細胞和組織就是這些器官的小區塊

​	

* span

通常會用來做區塊或者是標籤內的細部變化，本篇會加入一點點的`css`來做講解

​	

## div

不囉唆直接參考 [`index.html`](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/Lesson_3/index.html) 實際例子：

我們幫 `div` 加一點顏色，只要在標籤裡面加入`style=""`就可以針對這個標籤進行`CSS`的修改，那要幫他加上的是背景顏色，所以會使用`background-color`所以整個加起來就是：

```html
<div style="background-color: rgb(98, 223, 216)">
   區塊一
</div>
```

​	

從範例上會發現變成兩個區塊了，只要在我們區塊內的標籤都會套用這個效果，和前面所分享過的標籤都一起加進來實際運用，會發現包在div裡頭的標籤都一起套用到`div`的`css`效果

```html
<div style="background-color: rgb(98, 223, 216)">
   區塊一
</div>
<div style="background-color: rgb(228, 146, 146)">
   區塊二
</div>
```

## 結果

![01_div.jpg](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/01_div.jpg)

![02_div.jpg](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/02_div.jpg)

​	

再來看兩個小例子，我們要做的是一個深灰色底白色字的網頁，這邊新增了一個`css`效果，字體顏色，我們要使用的屬性是 **color**，利用 `; `將兩個屬性分開 **`style="background-color:#3b3b3b;color:#fff"`**

​	

1. 第一個做法：利用 **div** 將我們的標籤都包起來套用

```html
  <div style="background-color: #3b3b3b; color: #fff">
    <h1>早安，晨之美</h1>
    <h2>魯廣眾</h2>
    <p>嘿!吃早餐阿!快點啦!</br>
      有好多好多早餐在這裡</br>
      在我們最熟悉的早餐店裡</br>
      不管你睡的多晚起的多晚</br>
      晨之美永遠在這裡歡迎光臨你
    </p>
    <p>
      對啊。對啊。對啊。對啊。
      </br>對啊。對啊。對啊。對啊。
      </br>對啊。對啊。對啊。對啊。
      </br>對啊。對啊。對啊。
    </p>
  </div>
```

## 結果

![03_div.jpg](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/03_div.jpg)

​	



2. 第二個做法： **不使用div**

```html
  <h1 style="background-color: #3b3b3b; color: #fff">早安，晨之美</h1>
  <h2 style="background-color:#3b3b3b;color:#fff">魯廣眾</h2>
  <p style="background-color:#3b3b3b;color:#fff">嘿!吃早餐阿!快點啦!</br>
    有好多好多早餐在這裡</br>
    在我們最熟悉的早餐店裡</br>
    不管你睡的多晚起的多晚</br>
    晨之美永遠在這裡歡迎光臨你
  </p>
  <p>
    對啊。對啊。對啊。對啊。
    <br style="background-color:#3b3b3b;color:#fff">對啊。對啊。對啊。對啊。
    </br>對啊。對啊。對啊。對啊。
    </br>對啊。對啊。對啊。
  </p>

```

## 結果

![04_div.jpg](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/04_div.jpg)

​	

#### 有什麼不一樣？
假設我們使用第一種方法使用`div`，就只需要在最外層的div加上style就好；但如果是第二種，就必須在每一個標籤上加上 style 是不是有一種做 **重複做輪子** 的感覺？而且還會一塊一塊的看起來不像同一個區域的東西一樣。

在最前面提過，我們會將網頁做區塊的分類 **header、content、footer** 再去切版，如果不使用`div`的話在製作的過程會很痛苦，而且也會造成下一個維護你專案的人的痛苦！！！

-----------------------------------


## span
通常 `span` 會包在 **標籤裡面做更細部的變化**，這邊就直接實作一個實際例子

```html
  <span style="background-color:#6cafee">span</span>
  <p style="background-color:#ecee69;">
    有好多好多早餐在這裡，
    <span>不管你睡的多晚起的晚，</span>晨之美永遠在這裡歡迎光臨你
  </p>

  <p style="background-color: #c4e79d">
    對啊。
    <span style="color:rgb(211, 29, 83)">對啊。</span>
    對啊。對啊。
    <br>對啊。對啊。對啊。
  </p>
```

​	

## 結果

![06_div.jpg](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/06_div.jpg)

這邊我們會發現一件事，`span` 不是一個區塊，雖然它的功用跟 `div` 看起來很像，
我們看這行**有好多好多早餐在這裡，不管你睡的多晚起的晚，晨之美永遠在這裡歡迎光臨你** ，
**不管你睡的多晚起的晚，**這行有使用 `span` 包起來，但是因為沒有對它下任何樣式修改所以他看起來並沒有變化。

​	

而以下，
**對啊。 對啊。 對啊。對啊。**
**對啊。對啊。對啊。**
用 `span` 包起來 **上面第二個對阿。** 變成紅色，但其他的文字並沒有跟著有任何改變，
這樣是不是有對 `div` 以及 `span` 有比較多的瞭解了呢？

​	

如果還是有一點似懂非懂，在一開始提到的定義再搭配這些範例看一次應該就非常有感囉～
**假設人體是一個網頁，那每個器官和部位對於人體來說就是一個一個區塊，那每個器官裡面都有細胞和組織，這些細胞和組織就是這些器官的小區塊**



# 常用標籤(三) _ ol、ul、li、如何使用開發者工具、超連結 a

-------------------------------------------------------

今天分享的 ol、ul、li 標籤超級無敵常用，常用程度僅次於 **div 跟 span**

​	

### 為什麼會很常用它？

當我們要設計數個連續長相的元件，像是一個**菜單的分類**的選單，就一定會用到 ul、li，如下：

#### 鬍鬚郭菜單
* 乳肉飯

* 大腸包滷肉

* 滷肉炒飯


### 那怎麼知道它是用ul li去做的？

我們先簡單的講解一下ol、ul、li，通常`li`都是被包在`ol`或是`ul`裡面

## 實例

```html
<body>
  <ol>
    <li>乳肉飯</li>
    <li>大腸包滷肉</li>
    <li>滷肉炒飯</li>
  </ol>

  <ul>
    <li>乳肉飯</li>
    <li>大腸包滷肉</li>
    <li>滷肉炒飯</li>
  </ul>

  <a href="https://www.youtube.com/watch?v=au2n7VVGv_c">點我連結到Post Malone - Psycho ft. Ty Dolla $ign</a>
</body>
```



## 結果

![06_ol](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/06_ol%E3%80%81ul%E3%80%81li.jpg)

這兩個最大的差別就在於一個是 **有序號(ol)**、**一個沒序號(ul)**，是不是很簡單明瞭？

-----------------------------------------

## 如何使用開發者工具
各大網站的選單是用 ul、li 做的，是去哪看到的呢？

這邊要開啟的是**開發者工具**，什麼是開發者工具呢？顧名思義就是方便我們開發網站用的工具，
每個瀏覽器都有，這裡是用 Google 的 Chrome ，請點擊 Chrome 右上方的的三個點點(功能設定)

![08_ol](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/08_ol%E3%80%81ul%E3%80%81li.jpg)

### 快捷鍵

> 選擇 更多工具 > 開發人員工具
>
> windows -> F12
> MAC -> option + command + i

按完 F12 有一大堆東西跑出來，我們今天只分享一個最基本的功能，剩下的等之後有用到在講會比較有印象
點擊，開發者工具左上角的 icon。

![10](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/10%20-%20%E9%80%99%E6%99%82%E5%80%99%E4%BD%A0%E7%9A%84%E6%BB%91%E9%BC%A0%E5%8F%AA%E8%A6%81%E7%A7%BB%E5%8B%95%E5%88%B0%E4%BB%BB%E4%B8%80%E5%80%8B%E5%85%83%E4%BB%B6%E4%B8%8A%E9%9D%A2%EF%BC%8C%E9%83%BD%E6%9C%83%E5%87%BA%E7%8F%BE%E4%B8%80%E5%B1%A4%E8%97%8D%E8%89%B2%E7%9A%84%E8%A6%86%E8%93%8B%E5%8D%80%E5%9F%9F.jpg)



這時候你的滑鼠只要移動到任一個元件上面，都會出現一層藍色的覆蓋區域

![11](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/11_%EF%BC%88%E6%A1%86%E8%B5%B7%E4%BE%86%E7%9A%84%E5%B0%8F%E5%B0%8F%E5%B0%8D%E8%A9%B1%E6%A1%86%E9%A1%AF%E7%A4%BA%E7%9A%84%E6%98%AF%E7%9B%AE%E5%89%8D%E7%9A%84%E6%A8%99%E7%B1%A4%E4%BB%A5%E5%8F%8ACSS%E7%9A%84class%E5%90%8D%E7%A8%B1%20(%E9%80%99%E5%BE%8C%E9%9D%A2%E5%88%86%E4%BA%AB)%20%E9%BB%9E%E4%B8%8B%E5%8E%BB%E5%BE%8C%EF%BC%8C%E9%96%8B%E7%99%BC%E8%80%85%E5%B7%A5%E5%85%B7%E6%9C%83%E8%87%AA%E5%8B%95%E5%B9%AB%E4%BD%A0%E8%B7%B3%E5%88%B0%E8%A9%B2%E5%85%83%E4%BB%B6%E7%9A%84html%E6%A8%99%E7%B1%A4%E4%BD%8D%E7%BD%AE%EF%BC%89.jpg)

框起來的小小對話框顯示的是目前的標籤以及`css`的`class`名稱 (這後面分享) 點下去後，開發者工具會自動幫你跳到該元件的html標籤位置，橘色的箭頭部分就是我們目前選取這個元件的標籤

![12](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/12_%EF%BC%88%E6%A9%98%E8%89%B2%E7%9A%84%E7%AE%AD%E9%A0%AD%E9%83%A8%E5%88%86%E5%B0%B1%E6%98%AF%E6%88%91%E5%80%91%E7%9B%AE%E5%89%8D%E9%81%B8%E5%8F%96%E9%80%99%E5%80%8B%E5%85%83%E4%BB%B6%E7%9A%84%E6%A8%99%E7%B1%A4%EF%BC%89.jpg)

​	

---------------------------------

### a 超連結

![13](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/13_%E7%A4%BA%E7%AF%84a%E9%80%A3%E7%B5%90.jpg)

**a** 簡單講就是**用來製作超連結的標籤**，有時候我也會利用 **a** 來製作按鈕用法

```js
<a href="想要連結過去的網址">文字</a>
```

我們來實際看例子

```js
<a href="https://www.youtube.com/watch?v=au2n7VVGv_c">點我連結到Post Malone - Psycho ft. Ty Dolla $ign</a>
```



### 結果

![14](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/14_%E6%96%87%E5%AD%97%E8%AE%8A%E6%88%90%E4%BA%86%E8%97%8D%E8%89%B2%E6%9C%89%E5%BA%95%E7%B7%9A%E7%9A%84%E7%8B%80%E6%85%8B%EF%BC%8C%E4%BB%A3%E8%A1%A8%E7%9B%AE%E5%89%8D%E4%BB%96%E6%98%AF%E4%B8%80%E5%80%8B%E9%80%A3%E7%B5%90%E6%88%91%E5%80%91%E4%BE%86%E7%94%A8%E9%96%8B%E7%99%BC%E8%80%85%E5%B7%A5%E5%85%B7%E7%9C%8B%E7%9C%8B.jpg)

文字變成了藍色有底線的狀態，代表目前它是一個連結我們來用開發者工具看看，是不是就跟我們上面分享的內容一樣呢？下回分享`table`的使用方法後就開始進入`CSS`的世界～～


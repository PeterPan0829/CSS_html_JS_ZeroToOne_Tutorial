# CSS _ 選擇器與優先權



由於 **CSS** 的屬性真的太多了所以我會以實際切版來做分享，	
先來個簡單的之後會分享按鈕樣式，期待一下～

-----------------------------------

## 選擇器

什麼是選擇器呢？	
簡單說，就是要去針對某個元件去做屬性的變換時所使用的工具。

先來一個基本的`style`格式，通常會將CSS的部分寫在 **head** 標籤裡面。

```html
<head>
  <title>CSS's World</title>
  <style>
    選擇器{
      屬性
    }
  </style>
</head>
```

------------------------------

## 元素選擇器

還記得前幾堂課程所分享的那些標籤嗎？		
我們可以直接利用**元素選擇器**去為所有的標籤去做**樣式修改**。	

### style

```html
  <style>
    div {
      background: #c9eb8c;
    }
    h1 {
      color: #910c2b;
    }
    p {
      color: #336d77;
    }
  </style>
```

### html

```html
<body>
  <div>
    <h1>早安，晨之美</h1>
    <p>嘿!吃早餐阿!快點啦!</br>
      有好多好多早餐在這裡</br>
      在我們最熟悉的早餐店裡</br>
      不管你睡的多晚起的多晚</br>
      晨之美永遠在這裡歡迎光臨你
    </p>
  </div>
  </br>
  </br>
  <div>
    <h1>晚安，詡唇每</h1>
    <p>
      對啊。對啊。對啊。對啊。
      </br>對啊。對啊。對啊。對啊。
      </br>對啊。對啊。對啊。對啊。
      </br>對啊。對啊。對啊。
    </p>
  </div>
</body>
```

### 結果

![20](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/20_%EF%BC%A3%EF%BC%B3%EF%BC%B3%E9%81%B8%E6%93%87%E5%99%A801.jpg)

因為針對標籤去設定屬性，所以整個`html`只要這個標籤有設定屬性那它就會去變更。

​	

--------------------------------

## class

class 大概是我們會最常用的選擇器，不管是什麼標籤，只要加上`class`就會幫你套上樣式。

### style
只要是`class`都會有一個` . `

```html
/*長寬各為40px，背景顏色為#c9eb8c*/
    .style{
      height: 40px;
      width: 40px;
      background-color:#c9eb8c;
    }
```

**html**

```html
 <div class="style">
    1
  </div>
  <div>
    <h1 class="style">2</h1>
  </div>
  <p>有好多好多早餐在這裡</p>
```

### 結果
在第一個 div 以及第二個 div 裡的 h1 下同一個 class 它就都會套用同樣的效果

![21](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/21_%EF%BC%A3%EF%BC%B3%EF%BC%B3%E9%81%B8%E6%93%87%E5%99%A802.jpg)



---------------------------

## ID

其實`id`的用法就跟`class`**差不多**，最不同的地方就是 **id 是不能重覆使用的**

```html
<div id="theID"></div>
```

我們將這個`div`標籤加上了`id`屬性，那麼`theID`這組`id`就是只有這一個 **div** 可以使用。
### 但是 class 可以一直重覆使用，所以通常會將「重覆樣式的元件」寫成class 讓我們可以用同一套樣式做修改。
```html
#theID{
/*屬性*/
}
```

### 「等等! Peter，那今天只是要針對div裡面的p去做改變而已呢？我不要改變全部的」

那只要這樣寫就可以了我們要div裡面的p對吧?

```html
div p {
/*屬性*/
}
```

這是一個 **層級的關係**，	
`div`是第一層`p`是第二層，單看你要使用什麼樣的選擇器。	
假設今天第一層是一個`class`或是`id`那底下有某一組你要使用的`class`或`id`、`元素`。

```html
/*在 className 這個 class 底下的 theId 這個 id */
.className #theId{
/*屬性*/
}
/*在 className 這個 class 底下的 所有p標籤*/
.className p{
/*屬性*/
}
/*在 theId 這個 id 底下的 所有h1標籤*/
#theId h1{
/*屬性*/
}
/*在 className 這個 clas s底下的 theId 這個 id 底下的 所有h1標籤*/
.className #theId h1{
/*屬性*/
}
```

-----------------------------------------------

# 優先權

是的，樣式也有所謂的優先權。	
標籤內的`style=""`的權限為最高的，再來是頁面內的`<style> `裡寫的樣式，最後是`外部連結引入的樣式`

### The Rule：標籤內的樣式 ==> 頁面內的樣式 ==> 外部引入的樣式

### 實例
### style
```html
  .style{
    height: 40px;
    width: 40px;
    background-color:#415c10;
  }
```
### html
```html
 <div class="style" style=" background-color:#c9eb8c;">
    1
 </div >
 <div class="style">
   <h1>2</h1>
 </div>
```

來仔細看原本的`class`的背景顏色都是設定為深棕綠色，	
而我也在標籤裡的`style`寫了**相同的屬性** `background-color`，因為標籤內的`style`的優先權比 `.class`高所以會以style內的為主。	

直接看**開發者工具** （忘記怎麼打開就複習一下前面的分享唷）	

![22](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/22_%EF%BC%A3%EF%BC%B3%EF%BC%B3%E9%81%B8%E6%93%87%E5%99%A803.jpg)

​	

再來是樣式內寫屬性的優先順序最後一個樣式屬性的權限會比之前的高。

### id > class
因為`id`不可重覆的關係所以它的優先權比`class`高，當兩個相衝突的時候會以`id`為主。

​	

### 最終大魔王 **!important**
假設使用了`!important`該屬性的優先權會被拉到最高，它會無視之前上面的優先權關係。

那當有`!important` 時，優先權就是依先後順序，跟其它選擇器的優先權規則一樣，所以除非必要不然最好少用`!important`。

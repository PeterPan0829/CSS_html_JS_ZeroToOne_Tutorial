# 版型設計切版(二)_基礎樣式2 _ 關於 hover 改變一下顏色！

### 選單的部分
![43](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/43_%E7%89%88%E5%9E%8B%E8%A8%AD%E8%A8%8821.jpg)

​	

屬性設定為這樣：
```css
.menu ul li {
    font-size: 1.3em;
    font-width:300;
    padding: 10px 30px;
    color: #ffffff;
}
```

**font-size**：設定字體大小 **1em** 為一般字體大小等同百分比，這邊因為要讓比一般字大一點所以使用1.3em

**font-width**：設定字體的粗細

**padding**：設定每個li的上下內距為10px、左右內距為30px

**color**：設定文字顏色為白色

​	

![43](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/43_%E7%89%88%E5%9E%8B%E8%A8%AD%E8%A8%8821.jpg)

初步看起就會像是上面的圖那樣。
今天要講的就是關於 **hover**，就是當我們**滑鼠移過去會出現的效果**，這裡先做一個就是滑過去以後會改變顏色，並且我們要讓它細緻一點，有一點漸變的感覺

​	

### 寫法
選擇器名字:hover{
/滑鼠移動過去以後要改變的屬性/
}

```css
.menu ul li:hover {
    background-color: #e29e9e;
    color: #4a4a4a;
}
```

當滑鼠移動到`<li>` 改變背景顏色`background-color： #e29e9e;`以及字的顏色`color： #4a4a4a;`	
依照目前的結果去做滑動效果會發現顏色是直接改變，這感覺對了但蠻生硬的。		
所以接下來我們要利用**transition**去顯示過度動畫。

​	

在`.menu ul li`裡加入 **transition: 0.25s;**
**0.25s** 代表時間

​	

### 完整CSS
```css
/*補title裡面字體的樣式*/
.menu .title span {
    font-size: 2em;
    color: #ffffff;
    margin-left: 20px;
}

.menu ul li {
    font-size: 1.3em;
    font-width:300;
    padding: 10px 30px;
    color: #ffffff;
    transition: 0.25s;
}

.menu ul li:hover {
  background-color: #c2c9a3;
  color: #4A4A4A;
}
```

以下是底部三個 **link** 的樣式（補充）	
這三個 **link** 分別要使用的有圓角、調整圖片x軸位置	
那我們 .link區塊必須新增 **text-align: center;** 用處是要讓我們的三個連結都置中	

```css
.menu .link div {
    height: 20px;
    width: 20px;
    display: inline-block;
    /*-----主要新增的樣式------*/
    border: 1px solid #ffffff;
    padding: 10px;
    border-radius: 50px;
    margin: 10px 10px;
   /*-----主要新增的樣式------*/
}
```

**border**：調整邊框的屬性，三個值分別為：**線條粗細**、**線條樣式**、**線條顏色**


### link的樣式
```css
.menu .link .fb {
    background: url('../img/facebook-logo.png') 15px no-repeat;
    background-size: auto 20px;
}
```

**background**：

1. 圖片路徑位置

2. y軸移動15px，簡單說就是讓他向右移動15px，如果要上下調整 只需要在後面再多加一個值就好

3. 不要重覆


剩下的兩個以此類推～

​	

### 完整CSS
```css
.menu .link {
    width: 100%;
    position: absolute;
    left: 0;
    bottom: 0;
    text-align: center;
}

.menu .link div {
    height: 20px;
    width: 20px;
    display: inline-block;
    border: 1px solid #ffffff;
    padding: 10px;
    border-radius: 50px;
    margin: 10px 10px;
}

.menu .link .fb {
  background: url('../img/facebook-logo.png') no-repeat;
  background-size: auto 20px;
}

.menu .link .github {
  background: url('../img/github-logo.png') no-repeat;
  background-size: 20px auto;
}

.menu .link .instagram {
  background: url('../img/instagram-logo.png') no-repeat;
  background-size: 20px auto;
}
```




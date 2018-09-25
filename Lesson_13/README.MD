# 版型設計切版(二)_基礎樣式2 _ hover 滑動效果顯示

​	

### hover

這個功能其實可以用 JavaScript 去做，
但是！也可以用純CSS的方式來顯示～

​	

首先是 html 的部分
我們先來做一個簡單的想法釐清，
還記得如果要做 **當滑鼠移動過去的時候改變樣式** 這個 **起手式** 就是這樣寫嗎？

```css
.button:hover {
 background-color:red;
}
```

講成中文就是 **class是套用button的標籤在滑鼠移動過去的時候會改變背景顏色為紅色**	
那現在要做的事情是顯示一個區塊A，區塊Ａ預設為不顯示，因為要滑過才顯示	
預設為不顯示很簡單就是 **display:none;**	
但是當 **button** 是被滑鼠滑過的 **狀態** 的時候，區塊Ａ就會顯示	

把這句話寫成 CSS 就是：

```css
.button:hover 區塊Ａ{
    display:block; /*將區塊顯示*/
}
```


那從之前講過的 **CSS選擇器** 可以知道區塊Ａ必須是包裹在 **button** 裡面的，所以 html 是這樣：
```html
  <div class="button">
    <span>嗨～滑我＞＜＂</span>
    <div class="hover">
      Pressure Test^^""
    </div>
  </div>
```

### 完整CSS
```css
body{
   background-color:#343434;
}
.button{
  width:100px;
  text-align: center;
  color:#fff;
  font-size:3em;
}
.button:hover .hover{
  display:block;
}
.hover{
  display:none;
  background-color:#ffb2b2;
}
```


### 結果
記得補上照片


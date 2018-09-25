# 彈出效果 _ animation

開始之前先想一下將球丟下去後在彈起來，
是不是會在空中停留一下下然後在掉下來？

​	

### 示意圖
![47gif](https://github.com/PeterPanTW/CSS_html_JS_ZeroToOne_Tutorial/blob/master/img/47.gif)

所以彈出的效果，其實就有點像是這樣

​	

上升後超出預設停留的位置一點點後再下降到停留的位置，就會造成一種他好像彈了一下的錯覺

​	

今天要利用的是 **animation** 來寫CSS動畫	
那在 **做任何動畫以前都必須先分析好影格**	
就有點想是我們在做 **gif動畫** 一樣	

​	

這邊分享一個工具，假設真的是一個顏色選擇障礙的人
可以使用這個網站 http://colorsupplyyy.com/app/
可以快速的配置一下範例


> icon 推薦網站 https://www.flaticon.com


### html
```html
  <div class="div">
    <div class="tool"></div>
    <div class="show"></div>
  </div>
```


**.div**：主要滑過的區塊
**.tool**：用來顯示按鈕形狀的div
**.show** : 彈出顯示的div

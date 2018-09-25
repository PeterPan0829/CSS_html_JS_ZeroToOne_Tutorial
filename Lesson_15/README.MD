# 切版_條列式訊息呈現

來把最後一個部分完成！

### 示意圖

圖片呢？？？？？？？？？？img/29_版型設計07（請記得換成自己的）.jpg

​	

複習一下 **html** 的部分

```html
    <div class="news">
      <div>最新文章</div>
      <ul>
        <li>文章1</li>
        <li>文章1</li>
        <li>文章1</li>
      </ul>
      <a href="#">more</a>
    </div>
```

讓我們先把這區變回白色
拿掉原本為了顯示用的淺藍色
也就是 **content** 以及 **news** 裡的`background-color`

圖片呢？？？？？？？？？？img/29_版型設計07（請記得換成自己的）.jpg



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
# 常用標籤(四) _ table（包含 tr、td、th、colspan、rowspan、caption）

這是常用標籤的最後一個主題，之後開始分享 **CSS3** 的用法

### table

### table = 一般表格
**如同字面的意思他就是表格，不知道多久以前的網頁貌似都是使用表格在做排版的**

那我們就直接來分享用法

```js
  <table border="1">
    <tr>
      <td>
        1
      </td>
      <td>
        2
      </td>
    </tr>
  </table>
```

**table** 標籤包住整個表格，在標籤裡面的 **border** 是我們用來設定表格的線框的
**tr** 是橫列
**td** 則是直行

### 結果

圖片呢？？？？？？？？？？img/15

### 合併欄位

那在製作表格的時候也很常用到合併的表格，那應該怎麼處理呢？
看實際例子，假設我們今天要製作的表格是長這樣

圖片呢？？？？？？？？？？img/16

先用上述一般表格來排列

```js
  <table border="1">
    <tr>
      <td>格子</td>
      <td>合併的欄位</td>
    </tr>
    <tr>
      <td>早餐</td>
      <td>午餐</td>
      <td>晚餐</td>
    </tr>
  </table>
```


### 結果
第一列的最後面是不是多了段空白？
那這時候在 **合併的欄位** 這一行的 **td** 裡面加上 **colspan="2"**
**colspan="2"** 這個的意思是代表它會橫跨兩個格子，你也可以解釋成它就是將兩個格子合併再一起

### 實例
```js
  <table border="1">
    <tr>
      <td>格子</td>
      <td colspan="2">合併的欄位</td>
    </tr>
    <tr>
      <td>早餐</td>
      <td>午餐</td>
      <td>晚餐</td>
    </tr>
  </table>
```

### 結果
圖片呢？？？？？？？？？？img/17

那如果是想要 **合併直行** 呢？那就要使用 **rowspan**

### 實例
```js
  <table border="1">
    <tr>
      <td rowspan="2">格子</td>
      <td colspan="2">合併的欄位</td>
    </tr>
    <tr>
      <td>早餐</td>
      <td>午餐</td>
    </tr>
  </table>
  ```

### 結果
圖片呢？？？？？？？？？？img/18


這邊再補充說明幾個標籤
**caption** 它是指我這整個表格的標題用法
**th** 是指我這個欄位的標題
### 實例
```js
  <table border="1">
    <caption>I'm Title!!!</caption>
    <tr>
      <th>格子</th>
      <th colspan="2">合併的欄位</th>
    </tr>
    <tr>
      <td>早餐</td>
      <td>午餐</td>
      <td>晚餐</td>
    </tr>
  </table>
```

### 結果
圖片呢？？？？？？？？？？img/19

有沒有發現利用 **th** 包起來的欄位變成加粗了變得比較明顯？
下一個 Lesson 就讓我們進入 **CSS** 的世界吧！！！！



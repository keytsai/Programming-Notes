# form

```markup
<form action="">
    <fieldset>
        <legend>contact US</legend>
        <p><label for="p1">Name:</label><input type="text" size="25" id="p1" placeholder="請輸入正確姓名 必填欄位" required></p>
        <p><label for="p2">Email:</label><input type="email" size="25" id="p2" placeholder="請輸入正確格式的電子郵件" required></p>
        <p><label for="p3">Phone:</label><input type="tel" id="p3" placeholder="請輸入行動電話"></p>
        <p><label for="p4">Web:</label><input type="url" id="p4" placeholder="請輸入您的網站網址"></p>
        <p><label for="p5">Birthday:</label><input type="date" id="p5"></p>
        <p><label for="p6">Order:</label><input type="number" id="p6" value="1" min="1" max="10" step="1"></p>
        <p><label for="p7">Product:</label><input type="text" id="p7" list="shopping"></p>
        <datalist id="shopping">
            <option value="LED"></option>
            <option value="DVD"></option>
            <option value="HDV"></option>
        </datalist>
        <p><label for="p8">Satisfied:<br>OK | GOOD | PERFECT<br></label><input type="range" id="p8" min="1" max="3" step="1"></p>
        <p><input type="submit" value="寫好送出"> <input type="reset" value="清除重填"></p>
    </fieldset>
</form>
```

![form](../../.gitbook/assets/2020-10-20-12-50-55%20%281%29.png)

## 說明

* 本範例表單輸入此行快速產生架構：`form>fieldset>legend{contact US}+(p>label+input)*6`
* 元素說明：

| 元素 | 說明 |
| :---: | :---: |
| fieldset | 用來對form表單中的控制元件做分組 |
| legend | 作為表單的標題，位於fieldset下的第一個 |
| datalist | 下拉表單，與list屬性配合 |

* 屬性說明：

| 屬性 | 說明 |
| :---: | :---: |
| required | 使欄位不得為空白 |
| placeholder | 讓欄位空白時顯示文字 |
| value | 設定初始值 |
| min | 設定最小值 |
| max | 設定最大值 |
| step | 設定每次增減值的單位數 |
| list | 下拉表單，與datalist標籤配合 |
| type | input元素的類型，詳下表格 |

* 類型\(type\)說明：

| 類型 | 說明 |
| :---: | :---: |
| text | 字元 |
| email | Email |
| tel | 號碼 |
| url | 網址 |
| number | 數量 |
| date | 日期（會有小月曆） |
| range | 可拉的範圍桿 |


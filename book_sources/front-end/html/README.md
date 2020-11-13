# HTML

## 網頁欄位架構、表格、form表單等的快速建立方式範例\(Emmet套件功能\)

* `table>(tr>td*3)*2`
* `form>fieldset>legend{contact US}+(p>label+input)*6`
* `header>h1+small^nav>a*4^video+#left>(h2+p*3)*4^#right>img*3+form^footer`
* `div>h1{NEWS}^div+div`

## HTML新標籤

### 頁面架構標籤

![html5NewTag](../../.gitbook/assets/2020-10-20-10-28-31%20%281%29.png)

#### 網頁範例

```markup
<!DOCTYPE html>
<html lang="zh-TW">

<head>
    <meta charset="UTF-8">
    <title>HTML5-頁面整合 請參考pageMix2.jpg 完成</title>
    <link rel="stylesheet" href="show.css">
</head>

<body>
    <!--
    header>h1+small^nav>a*4^video+#left>(h2+p*3)*4^#right>img*3+form^footer
    -->
    <header>
        <h1>親近自然 擁抱美麗</h1>
        <small>讓我們迎向大自然 充滿笑聲迴盪在每一天</small>
    </header>
    <nav>
        <a href="">露營禮節</a>
        <a href="">器材準備</a>
        <a href="">地點推薦</a>
        <a href="">聯絡我們</a>
    </nav>
    <video src="movie2.mp4" autoplay loop controls muted></video>
    <div id="left">
        <h2>露營禮節</h2>
        <p>營帳規格</p>
        <p>野炊安全</p>
        <p>入山活動</p>
        <h2>器材準備</h2>
        <p>細節規劃</p>
        <p>任務分配</p>
        <p>環境安全</p>
        <h2>地點推薦</h2>
        <p>北部地區</p>
        <p>中部地區</p>
        <p>南部地區</p>
        <h2>連絡我們</h2>
        <p>來訪地圖</p>
        <p>留言討論</p>
        <p>即時通訊</p>
    </div>
    <div id="right">
        <img src="c1.jpg" alt="">
        <img src="c2.jpg" alt="">
        <img src="c3.jpg" alt="">
        <form action="">
            <fieldset>
                <legend>contact US</legend>
                <p><label for="p1">您的姓名：</label><input type="text" size="25" id="p1" placeholder="請輸入正確姓名 必填欄位" required></p>
                <p><label for="p2">電子郵件：</label><input type="email" size="25" id="p2" placeholder="請輸入正確格式的電子郵件" required></p>
                <p><label for="p3">聯絡電話：</label><input type="tel" id="p3" placeholder="請輸入行動電話"></p>
                <p><label for="p5">出生日期：</label><input type="date" id="p5"></p>
                <p><label for="p7">居住地區：</label><input type="text" id="p7" list="shopping"></p>
                <datalist id="shopping">
                    <option value="北部"></option>
                    <option value="中部"></option>
                    <option value="南部"></option>
                </datalist>
                <p><label for="p8">露營經驗:<br>陌生 | 新手 | 老經驗<br></label><input type="range" id="p8" min="1" max="3" step="1"></p>
                <p><input type="submit" value="送出"> <input type="reset" value="重設"></p>
            </fieldset>
        </form>
    </div>
    <footer>Happy Camp &copy;Copyright 2020 by Your LOGO
        - XXXX@gmail.com</footer>
</body>

</html>
```

![htmlEx](../../.gitbook/assets/2020-10-20-14-36-12%20%281%29.png)

### figure, figcaption

* figure:獨立內容區段描述
* figcaption:獨立內容區段描述標題說明

```markup
<figure style="float:left;">
    <img src="v1.jpg" alt="">
    <figcaption>稻田</figcaption>
</figure>
```

## 影音標籤

```markup
<video autoplay loop controls muted poster="c1.jpg">
    <source src="movie.mp4">
    <source src="movie2.mp4">
    <source src="movie.mp4">
</video>
```


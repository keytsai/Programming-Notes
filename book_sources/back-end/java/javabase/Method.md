# 使用方法

## 宣告static方法和變數

- 若在屬性或方法前加上static修飾詞，則該屬性或方法使用時就不需要再透過物件生成
  - 亦即直接使用類別，就能呼叫static方法和變數

### 沒有static時的困境

### 使用static解決問題

```java
package course.c10;

public class Circle1 {

    private double radius;
    static final double PI = 3.1415926;

    public void setRadius(double r) {
        this.radius = r;
    }
    // 
    public double getArea() {
        return this.radius * this.radius * PI;
    }

    // 此為公式，結果只和輸入參數有關
    static double areaFormula(double r) {
        return r * r * PI;
    }

    public static void main(String[] args) {

        System.out.println(Circle1.PI);

        // 圓半徑為1，求面積
        System.out.println(Circle1.areaFormula(1));

        // 圓半徑為10，求面積
        System.out.println(Circle1.areaFormula(10));

    }

}
```

### static宣告的意義

- 每個類別只載入一次，故類別成員在JVM裡是唯一存在
- 物件成員可以呼叫類別成員
- 類別成員不能出叫物件成員

定義在類別內的所有屬性和方法分兩類：

1. 未使用static宣告
   - 必須先產生物件，再使用物件參考(遙控器)去呼叫
   - 無static宣告的欄位和方法稱為**物件成員(object member)**
2. 使用static宣告
   - 因為只用類別名稱就可以呼叫方法和欄位，因此稱有static宣告的欄位和方法為**類別成員(class member)**

### static宣告的時機

```java
public class Circle2 {

    private double radius;

    public void setRadius(double r) {
        this.radius = r;
    }

    public double getArea() {
        return areaFormula(this.radius);
    }

    // 此為公式，結果只和輸入參數有關
    static double areaFormula(double r) {
        return r * r * Math.PI;
    }

}
```

## 建立多載的方法

### 方法的簽名

- 方法名稱及參數合併稱為方法簽名(method signature)
- 就像用簽名識別身份，方法不只用方法名稱識別，還要加上參數
- 認定方法參數是否相同有三個考量：
  1. 數量
  2. 順序
  3. 型別

### 方法的多載

>同一個類別內，若有方法名稱相同，但簽名不同(否則無法編譯)，就稱為多載(Overloading)

使用時機：
若類別內有多個方法功能相近，只是傳入的參數型態、數量不同，就可以使用多載進行coding

## 變數值的傳遞

### 變數值傳遞的發生場景

- Java在兩種情況時需要傳遞(pass)變數/參數：
  1. 由指定運算子「=」右側，將值(value)傳遞給左側變數
  2. 透過方法宣告的參數，將值由呼叫者(caller)方法傳遞進入工作者(worker)方法中
- Java使用「Pass by Value」來傳遞變數/參數

### Pass by Value

1. 參考型別
   - 若變數屬於參考型別，則複製物件參考(遙控器)後進行傳遞。複製前後雖然是不同遙控器，但指向同一物件
![參考型別資料傳遞記憶體配置](/.gitbook/assets/2020-11-12-23-11-02.png)
2. 基本型別
   - 因為沒有遙控器的概念，因此是直接複製變數值，如同影印機複製原稿後產生副本，兩者各自獨立
![基本型別資料傳遞記憶體配置](/.gitbook/assets/2020-11-12-23-09-45.png)
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

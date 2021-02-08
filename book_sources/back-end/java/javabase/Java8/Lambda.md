# Lambda

## Lambda精神

- 不需要為了呼叫一個方法而設計一個完整類別及物件，直接看到方法內容
- 「=」左邊仍然是以介面作為型別宣告變數，但右邊則由原來的「類別定義」降格為「方法定義」
- Lambda的目的即爲用「方法定義」取代「類別定義」

## 包含三個部分

1. 方法參數
   - 參數的型別宣告可省略
   - 若只有單一參數且已省略型別宣告，則可以再省略()

2. 箭頭符號
3. 方法內容
   - 有{ }：和一般方法內code相同，例如：
     - 若有回傳須加return
     - 每行code以「;」隔開
     - 運算式或表示式須將結果指定給變數，如boolean a = (1<3)
   - 無{ }：
     - 不能加return(因為Java會自動判斷Functional Interface上宣告的抽象方法有沒有回傳)
     - 只有一行code，不需也不能使用「;」斷行

### 語法Ex

| 舉例                                     | 結果 | 說明                                 |
| ---------------------------------------- | ---- | ------------------------------------ |
| `(int x, int y) -> x + y`                | OK   |                                      |
| `(x, y) -> x + y`                        | OK   |                                      |
| `(x, y) -> {System.out.println(X +y );}` | OK   |                                      |
| `(String s) -> s.contains("word")`       | OK   |                                      |
| `s -> s.contains("word")`                | OK   | 只有一個參數可省略()                 |
| `() -> true`                             | OK   |                                      |
| `a, b -> a.startsWith("test")`           | NG   | 2個以上參數則()不能省略              |
| `a -> { a.startsWith("test"); }`         | OK   | 方法必須是void                       |
| `a -> { return a.startsWith("test") }`   | NG   | 有{}則code要有「;」            |
| `(a, b) -> {int a = 0; return 5;}`       | NG   | 方法內容的區域變數名稱不能和參數相同 |
| `(a, b) -> {int c = 0; return 5;}`       | OK   |                                      |

### 功能性介面 functionalInterface

搭配`@functionalInterface`annotation 可限定該介面只有一個方法

## 內建的Functional Interface

1. 評斷型(Predicate)：使用泛型傳入參數，且回傳boolean
2. 消費型(Consumer)：使用泛型傳入參數，且沒有回傳(void)
3. 功能型(Function)：將傳入的參數由T型別轉換成U型別
4. 供應型(Supplier)：如同工廠方法，提供T型別的物件

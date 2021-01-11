# 使用封裝和建構子

- 封裝：用來資訊隱藏、實現多型的必要手段
- 建構子：會在物件建構過程中被Java呼叫，故名。主要用來初始化物件的屬性欄位

## 使用建構子

### 建立建構子

建構子和類別成員「方法」的宣告和實作方式都很像，但有關鍵性的不同：

1. 建構子名稱必須和class名稱一樣
2. 沒有回傳，也不是void
3. 建構子若要多載，只能用不同參數創建

#### 語法

```java
[modifiers] class ClassName {
    [modifiers] ClassName ([arguments]){
        code_block
    }
}
// 第一個ClassName是類別名稱
// 第二個ClassName是建構子名稱
```

### 使用建構子建立新物件

- 參考型別物件建立的第二步驟實體化的語法為`new ClassName();`
  - 在new關鍵字後面的類別名稱即為建構子
  - 故所謂實體化，就是使用new關鍵字來呼叫建構子，完成記憶體空間heap裡的實體建立
- 若未在類別中建立建立建構子，Java會預設一個無參數的建構子，可直接使用
- 但若已建立過建構子，則Java即不提供預設建構子，此時以下呼叫就會編譯失敗：
`Book b1 = new Book();`
- 已建立其他建構子若仍需使用無參數建構子就要自行建立
- chaining constructors:建構子之間(overloading)若要互相呼叫，需使用「this」關鍵字加上參數
- [chaining constructors範例](Shirt2.java)

### 各級存取權限比較

|           | 同class | 同package | 不同package但須為子類別 | 不設限 |
| --------- | :-----: | :-------: | :---------------------: | :----: |
| private   |    Y    |           |                         |        |
| default   |    Y    |     Y     |                         |        |
| protected |    Y    |     Y     |            Y            |        |
| public    |    Y    |     Y     |            Y            |   Y    |

## 熟悉複寫規則

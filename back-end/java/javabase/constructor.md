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
  - 在new關鍵字
# Array

## 一維陣列與二維陣列

### 陣列的基本定義

- 為一種容器物件(container object)，可裝載多個且單一型態的基本型別或參考型別
- 陣列裡的內容物稱為成員(element)
- 建立時必須指定長度，即成員數量；建立後長度即不能改變
- 陣列的成員使用數字化的索引(index)存取，**第一個成員的index為0**

### 建立一維陣列

陣列也是物件，因此建立陣列的完整程序也分下列三部分：

- 第一部分：宣告

```java
type [] array_identifier;
// type:陣列的成員型別
// []:表示宣告陣列
// array_identifier:陣列名稱
```

- 第二部分：建構實體

```java
array_identifier = new type [length];
```

- 第三部分：初始化

```java
array_identifier[index] = value;
// index:成員位置，從0開始，最大長度為「長度 - 1」
```

- 可將上述三個程序一次完成(前提為程式碼不能分行)：

```java
type [] array_identifier = {成員以","區隔};
```

## ArrayList類別

### 陣列的缺點

陣列無法自動增加長度，有諸多不便：

1. 紀錄每個加入陣列的元素的索引
2. 追蹤並記錄陣列長度
3. 若長度不足，則必須建立一個足夠長度的新陣列，並將原陣列成員逐一複製過去，再捨棄原陣列

### ArrayList類別簡介

1. 只存放參考型別的物件，不接受基本型別；但可以改用基本型別的包覆類別
2. 有許多方法可以管理成員物件：add()、get()、remove()、indexOf()等
3. 建構ArrayList物件時不需要設定長度大小，當需要加入更多成員物件時，將自動成長
4. 在建構ArrayList物件時可設定initial capacity，但不強制

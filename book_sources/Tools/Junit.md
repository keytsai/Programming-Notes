# JUnit

## JUnit四大核心

1. TestCase / 測試案例
   - @Test
   - @Before — 在每個Test Method之前都會執行一次。
   - @After — 在每個Test Method之後都會執行一次。
   - @BeforeClass — 每個Test Class建構者執行後都會執行一次。
   - @AfterClass — 每個Test Class建構者執行後都會執行一次。
   - @Ignore — 忽略此單元測試，(若在單元測試class中方法沒加上Ignore，JUnit會執行失敗)
2. TestResult / 測試結果
3. TestSuite / 測試組合
4. Assert / 斷言(參閱如下：Assert常用API)

## Assert常用API

```java
assertEquals
// 判斷2個物件是否相等

assertNotEquals
// 判斷2個物件是否不相等

assertTrue
// 驗證是否為真

assertNull
// 驗證物件是否為null

assertNotNull
// 驗證物件是否不為null

assertArrayEquals
// 驗證陣列是否相同
```

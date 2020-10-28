# Servlet Life Cycle

## 四個生命週期

### 創建實體

* Servlet Reloading \(Servlet 重載入\) -&gt;**例外**
* Load on Startup \(啟動時載入\) -&gt;**例外**

### 初始化

* Init Parameter \(初始參數\)

### 服務

* Persistence vs Synchronization
* Single Thread Model \(單緒模型\)\(Deprecated\)

### 卸載

* Initial & Destroy \(協同運作\)

## 生命週期基本概念（測試）

![servlet life cycle](../../../.gitbook/assets/2020-10-28-10-49-03%20%281%29.png) ![servlet life cycle](../../../.gitbook/assets/2020-10-28-10-52-55%20%282%29.png)

* Servlet container: 替我們建立servlet實體，並由其控制呼叫servlet的`init()`, `service()`, `destroy()`等方法，以管理servlet的生命週期
* 程式設計師：則藉由提供上述方法之實作，予以控制該servlet物件及與該物件相關之resource

  

![&#x7B2C;&#x4E8C;&#x9801;&#x6E2C;&#x8A66;](../../../.gitbook/assets/2020-10-28-11-41-03.png)

![](../../../.gitbook/assets/2020-10-28-11-01-03%20%281%29.png)


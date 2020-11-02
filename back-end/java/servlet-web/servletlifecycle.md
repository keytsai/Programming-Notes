# Servlet 生命週期

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

## 生命週期基本概念

![servlet life cycle](https://github.com/keytsai/Software-Development/tree/4647e580ce8226a39d489e531d3f8ca7f1786338/back-end/.gitbook/assets/2020-10-28-10-49-03.png) ![servlet life cycle](https://github.com/keytsai/Software-Development/tree/4647e580ce8226a39d489e531d3f8ca7f1786338/back-end/.gitbook/assets/2020-10-28-10-52-55.png)

* Servlet container: 替我們建立servlet實體，並由其控制呼叫servlet的`init()`, `service()`, `destroy()`等方法，以管理servlet的生命週期
* 程式設計師：則藉由提供上述方法之實作，予以控制該servlet物件及與該物件相關之resource

![1/2](https://github.com/keytsai/Software-Development/tree/4647e580ce8226a39d489e531d3f8ca7f1786338/back-end/.gitbook/assets/2020-10-28-11-01-03.png)

![2/2](https://github.com/keytsai/Software-Development/tree/4647e580ce8226a39d489e531d3f8ca7f1786338/back-end/.gitbook/assets/2020-10-28-11-41-03.png)

## 背景執行緒

![&#x80CC;&#x666F;&#x57F7;&#x884C;&#x7DD2;](../../../.gitbook/assets/2020-10-30-15-56-42.png)


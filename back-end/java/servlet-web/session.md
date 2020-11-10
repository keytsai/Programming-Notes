# Session機制

## 什麼是Session

- 是一種紀錄用戶端狀態的機制
- 儲存在伺服器上
- Session相當於程式在伺服器上建立的一份客戶檔案，客戶來訪時只需查詢客戶檔案表即能追蹤

## 實現使用者登入

- 對應的類別為javax.servlet.http.HttpSession類別
- 每個來訪者對應一個Session物件，所有該客戶的狀態資訊都儲存在這個Session物件裡
- Session物件在用戶端第一次請求伺服器時建立
- Session是一種key-value屬性對，透過`getAttribute(String key)`及`setAttribute(String key, Object value)`方法讀寫客戶狀態資訊
- 透過`request.getSession()`獲得該客戶的Session，如：

```java
// 獲得Session物件
HttpSession session = request.getSession();

// 設定Session中的屬性
session.setAttribute("loginTime", new Date());

// 獲得Session屬性
out.println("登入時間為：" + (Date)session.getAttribute("loginTime"));
```

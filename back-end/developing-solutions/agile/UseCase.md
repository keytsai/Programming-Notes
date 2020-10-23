# Use Case & Actor

## Use Case Model

使用案例模型包括：

- 業務流程描述：Activity Diagram
- 使用者需求與系統功能：Use Case Diagram
- 使用案例事件流程：Use Case Description
- 使用者故事及驗收測試：User Story and Acceptance Test
- 使用案例情節：Activity Diagram
- UI設計：User-Interface Prototype

## Use Case 符號

![use case](images/2020-10-23-16-03-49.png)

## 使用案例注意事項

1. 使用案例之名稱通常是一個動詞片語
![use case](images/2020-10-23-16-14-47.png)
2. 使用案例間之關係通常只有三種：
   - 一般化
   - 包含
   - 擴充
**不能有表現流程、順序等關係出現**
![use case](images/2020-10-23-16-13-47.png)
↑應以購物車呈現

3. 使用案例應為EBP(Elementary Business Process)層級
![use case](images/2020-10-23-16-27-06.png)

## Actor

### Actor 符號

![use case](images/2020-10-23-16-34-52.png)

- 參與者為達到某項特殊目的，在系統之內所執行的一連串行動
- 對系統而言，使用者可以扮演的角色；或是存在系統之外的一個實體，例如： 另一個系統或是一個資料庫
- 參與者是在**系統之外**，但又與系統有關之實體
- 若參與者是人類，UML是以人形符號來表現；否則為增加視覺效果，可以使用 UML擴充機制中之造型 (stereotype)機制來表現
- 參與者與使用案例間是以關連(Association)連接，代表資料之傳送與接收

### 參與者注意事項

1. 參與者間可以有**一般化**(Generalization)之關係，參與者間不必有其他關係存在，因為那已是系統之外的部份
![use case](images/2020-10-23-16-38-42.png)
2. 參與者應是使用者可以扮演的角色，而非特定之人
![use case](images/2020-10-23-16-39-01.png)
3. 參與者是角色，而非職務
![use case](images/2020-10-23-16-39-22.png)

## Use Case Diagram

### 使用案例圖注意事項

1. 使用案例圖沒有階層性
![use case](images/2020-10-23-16-46-26.png)
2. 使用案例圖中可用套件符號來表示使用案例間之相關性
![use case](images/2020-10-23-16-46-43.png)

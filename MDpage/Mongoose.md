# Mongoose
MongoDB 的 ODM (將JS object轉換成document)
## 好處
- 更方便地將資料庫操作和應用程序邏輯分離開來，從而使代碼更加易於維護。
## 基本操作概念
1. 透過 Schema 定義 MongoDB 文檔的結構、屬性名稱、類型、驗證規則等，同時也可以在 Schema 中定義靜態方法(static)和實例方法(instance)。
2. 使用 Schema 創建 Model，代表 MongoDB 集合的類 (class)。
3. 兩種方法會被添加到 Model 的原型中，而非直接添加到 Model 本身。
4. 可想像 Schema 定義了文件的結構和使用規則（方法），而文件（ Model ）則是資料的容器，而實例（document instance）則是在容器內具體存儲的資料。

- 實例方法（instance method）可以對這些資料進行操作和管理。
- 靜態方法（static method）則直接針對文件(Model)進行操作，例如新增、查詢和修改等，並不需要看到具體的資料(實例)。
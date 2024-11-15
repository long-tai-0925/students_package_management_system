# 學生包裹管理系統
## 分兩個網頁

> ### 學生用

### 顯示資訊：
標題；
日期、學號、姓名、{樓層、寢室、床位}(2FD3-4)、類型(信件/掛號/包裹)、狀態(已領取、未領取)

範例：
|日期|學號|姓名|寢室|類型|狀態|
|----|----|----|----|----|----|
|{日期}|{學號}|{姓名}|{樓層、寢室、床位}|{類型}|{狀態}|

### 資訊存放：
學號、姓名、{樓層、寢室、床位}(2FD3-4)：
```students_info.json```  
日期、類型(信件/掛號/包裹)、狀態(已領取、未領取)：
```students_package.json```

### 主要功能：
顯示學生包裹資訊，方便學生查詢有沒有包裹，並前往領取，  
若包裹狀態為已領取則隱藏。


> ### 管理用
### 顯示資訊：
標題； 日期、包裹編號、學號、姓名、{樓層、寢室、床位}(2FD3-4)、類型(信件/掛號/包裹)、狀態(已領取、未領取)

範例：
|日期|編號|學號|姓名|寢室|類型|狀態|
|----|----|----|----|----|----|----|
|{日期}|{編號}|{學號}|{姓名}|{樓層、寢室、床位}|{類型}|{狀態}|

### 資訊存放：
學號、姓名、{樓層、寢室、床位}(2FD3-4)：
```students_info.json```  
日期、包裹編號、類型(信件/掛號/包裹)、狀態(已領取、未領取)、包裹編號：
```students_package.json```

### 主要功能：
設定學生包裹資訊，方便管理員管理包裹，並編輯或刪除資訊，  
設定簡易登入功能，  
防止惡意串改，並且填入學號後自動填入```學號、姓名、{樓層、寢室、床位}(2FD3-4)```，  
並再由管理員接手填入```日期、包裹編號、類型(信件/掛號/包裹)、狀態(已領取、未領取)```，


## 目前有的檔案：
```students_info.json```
```json
[
    {"id": "000001", "name": "鄧紫棋", "floor": "7", "room": "B1", "bed": "6"},
    {"id": "000002", "name": "鄧紫棋", "floor": "3", "room": "B3", "bed": "6"},
    {"id": "000003", "name": "趙麗穎", "floor": "4", "room": "C1", "bed": "4"},
    {"id": "000004", "name": "吳彥祖", "floor": "6", "room": "G2", "bed": "3"},
    {"id": "000005", "name": "林俊傑", "floor": "6", "room": "C1", "bed": "4"}
    //...
]
```

```students_package.json```
```json
[
    {
        "id": "000001",
        "packageType": "包裹",
        "status": "未領",
        "number" : "u0001"
    },
    {
        "id": "000002",
        "packageType": "信件",
        "status": "已領",
        "number" : "u0001"
    },
    {
        "id": "000003",
        "packageType": "包裹",
        "status": "已領",
        "number" : "u0001"
    }
    //...
]
```

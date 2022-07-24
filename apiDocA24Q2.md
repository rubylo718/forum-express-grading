# A24-Q2 API文件練習 #

## `GET api/restaurants `

### **說明** 

取得全部餐廳資料

### **Parameters**    
No

### **Available Query Strings**
attribute | Description
--- | ---
`limit` | 每頁顯示資料筆數 Optional. Default: `10`
`page` | 顯示第幾頁 Optional. Default: `1`
`orderBy` | 資料排序方法 Optional. (Valid value: `latest`, `oldest`. Default: `latest`.)
`categoryId` | 依照餐廳類別的id篩選資料 Optional. Default: `null`

### **Request Body**

No

### **Example Response**

* Success | Status code: 200
```JSON
{   
    "restaurants": [
        {
            "id": 401,
            "name": "Darnell Heathcote",
            "tel": "(577) 417-6732",
            "address": "488 Schulist Forge",
            "openingHours": "08:00",
            "description": "sed",
            "image": "https://abc.def",
            "viewCounts": 22,
            "createdAt": "2022-07-14T03:58:08.000Z",
            "updatedAt": "2022-07-17T09:50:36.000Z",
            "categoryId": 22,
        }, 
        // more restaurants...
    ]
}
```
* Failure | Status code: 404
```json
{
  "status": "error",
  "message": "Data not found!"
}
```


***

## `GET api/restaurants/:id`

### **說明** 

取得一筆餐廳資料

### **Parameters**   

param | Description
--- | ---
`id` | 欲取得的餐廳id. Required.

### **Request Body**
No

### **Example Response**
* Success | Status code: 200
```json
{
        "id": 401,
        "name": "Darnell Heathcote",
        "tel": "(577) 417-6732",
        "address": "488 Schulist Forge",
        "openingHours": "08:00",
        "description": "sed",
        "image": "https://abc.def",
        "viewCounts": 22,
        "createdAt": "2022-07-14T03:58:08.000Z",
        "updatedAt": "2022-07-17T09:50:36.000Z",
        "categoryId": 22
}
```
* Failure | Status code: 404
```json
{
  "status": "error",
  "message": "Data not found!"
}
```



#WEB js exercise
在這次的練習，可以體驗 js 如何在文件上處理資料的輸入與輸出。請打開`index.html` 並編輯 js/js.js 以完成以下要求。

注意，以下標記是說明文件寫法：

```javascript
// 代表 validate 方程式需要輸入一個屬性為 string 變數 inputValue ，執行結束會回傳一個 boolean，
function validate (inputValue:string) -> Boolean
// 真正的寫法會是以下
function validate (inputValue){
	//...
	return false ;
}
```
# Requirement

## 1.驗證使用者輸入

##### 1-1.實作 validate 方程式
```javascript
function validate (inputValue:String) -> Boolean
// 當 inputValue 長度大於 3 的時候回傳 true(有效) 否則 false
```

##### 1-2.在 todoInputEle 上監聽 input 事件，運用 validate 方程式檢查使用者輸入的 value 是否有效
```javascript
/*若有效則執行*/ validateHintEle.className = "has-success"
/*否則*/ validateHintEle.className = "has-error"
```
___

## 2.點選新增按鈕時，儲存資料並顯示元件()

##### 2-1.將新增的 TODO 用 object 表示（以下以變數`todoData`說明)，並存進陣列`todoDataArray`裡面
* 需有[敘述文字]以及[完成與否]兩屬性(物件的 key 請自己命名)。

##### 2-2. 用上一步驟的 object 裡的資料 創建 todoElement
* 必須要有以下結構
```html
//如果他的[完成與否]狀態為未完成，結構如下
<a href="#" class="list-group-item">TODO的敘述文字</a>
//如果他的[完成與否]狀態為完成，則結構如下
<a href="#" class="list-group-item list-group-item-success">TODO的敘述文字</a>
```

##### 2-3. 為此 todoElement 監聽 click 事件，觸發時請執行以下行為：
```javascript
// 實作1. 將對應的 `todoData` [完成與否] 值設定為完成狀態(true)
// 實做2. 呼叫下面的方程式
updatetodoListEle(todoDataList);
```

##### 2-4.將此 todoElement 顯示到 todoListEle 裡面。

##### 2-5.把使用者輸入的所有資料都存起來
```javascript
想辦法將 todoDataList 存進  localStorage
```

___

## 3. 網頁重新整理後 資料能重現

##### 3-1.將步驟 2-2 變成一個 createElement 方程式
```javascript
function createElement (todoData:Object) -> Element
```

##### 3-2.實作方程式
```javascript
function updatetodoListEle (todoDataList:Array) -> undefined
// 清空 todoListEle 內的所有子元素
// 運用`createElement` 創建 todoDataList 裡的每一筆 todoData 的 `Element`
```

##### 3-3. 讀取並顯示 localStorage 裡的資料

___





## 會用到的 API

```javascript
document.createElement()

// 拿到 input 得值
document.getElementById("<input element id>").value  

// HTMLElement 的 API
document.getElementById("<whatever you want>").className = string : String
document.getElementById("<whatever you want>").appendChild(  Element)

// hyperlink element 的 API
document.getElementById("<anchor element id>").href // 設定超連結

// array 新增子物件
[].push (  item : anyType )
[].length // 取得 Array 裡面物件的數量

// 關於儲存資料
localStorage.setItem( key : string , value : String)
JSON.stringify( object : Object) ;
JSON.parse ( JSON_String : String )

// 拿取每一個物件
for 迴圈
Array.prototype.forEach()
```





## 剩餘說明
```javascript
function validate (inputValue:string) -> Boolean
```
代表輸入一個屬性為 string 變數 inputValue 會回傳一個 boolean

#### 文件中的 JS 與網頁相關的 API

[DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document) , [HTMLInputElement](https://developer.mozilla.org/zh-TW/docs/Web/API/HTMLInputElement) ,
[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)

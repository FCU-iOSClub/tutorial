# 收集、切換、重複

挑戰：定義一個用於重複模式的函數。

## 簡介

在這項挑戰中，你需要收集多顆寶石，每顆寶石旁邊都有一個開關。

與其重複你在上一個關卡中使用的指令模式，倒不如編寫一個新的函數，其中包含現有的指令來處理每對寶石與開關的組合。

在這項挑戰中，你可以為你的函數任意命名。為函數命名並加以定義之後，透過輸入函數名稱來呼叫函數，就像呼叫所有其他使用過的函數一樣。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/5e7e4e70-cca2-478e-3b25-f44c6e0a6700/public)

## 講解

仔細觀察這關卡，可以發現，每個寶石與開關的組合都是一樣的，只要寫一個函數，然後重複呼叫它 4 次就可以了。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func pickPlace() {
    moveForward()
    collectGem()
    moveForward()
    toggleSwitch()
    moveForward()
}
pickPlace()
turnLeft()
pickPlace()
moveForward()
turnLeft()
pickPlace()
turnLeft()
pickPlace()
```

## 後記

到這裡，你已經熟悉了創建屬於自己的函數的方法！下一關，你要熟練的使用到目前為止你已經學到的所有技巧，趕快前往挑戰！

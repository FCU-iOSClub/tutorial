# 寶石農場

挑戰：將多個模式分解成函數和迴圈。

## 簡介

在這項挑戰中，你需要收集寶石並且打開開關。首先，你需要辦識收集寶石和啟動開關的模式。
然後，你要為每一種模式編寫一個函數，並計算出需要使用迥圈呼叫那些函數的次數。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/53fdd469-c3ce-48f9-de17-b38464d2cb00/public)

## 講解

首先，思考一下這項挑戰中你能分解成函數的所有任務。

如何使用 for 迴圈來重複執行你編寫的一組函數呢？

這是一個挑戰關卡，因此不提供解決方法。自己設計一個方案來通關吧，這樣才能強化程式設計的技巧。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func turnAround() {
    turnLeft()
    turnLeft()
    moveForward()
    moveForward()
}
func solveRow() {
    turnRight()
    moveForward()
    collectGem()
    moveForward()
    collectGem()
    turnAround()
    moveForward()
    toggleSwitch()
    moveForward()
    toggleSwitch()
    turnAround()
    turnLeft()
    moveForward()
}
for i in 1...3 {
    solveRow()
}
```

## 後記

真是不可思議！看看你的程式設計者之路進展有多快！你掌握了秘訣：將看似困難的問題分解成小問題，然後將簡單的解決方法組合成可重複呼叫的函數。

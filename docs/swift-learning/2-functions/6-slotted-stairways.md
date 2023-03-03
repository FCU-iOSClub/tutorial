# 嵌入式階梯

目標：透過多個函數來分解一個解決方法。

## 簡介

正如你剛剛學到的一個十分有用的方法就是，定義一個函數來完成一個小的任務，然後在另一個函數中呼叫此函數來完成較大的任務。

這種做法能讓你的程式碼變得更為易讀，因為你可以依據函數的目的來為函數命名；例如`turnAround()`。同時，這也簡化了編寫程式碼的過程，因為在你編寫一個函數來完成較大的任務之後，你不再需要考慮單獨的指令。

1. 執行程式碼來查看呼叫 `solveRow()` 時會發生什麼、
2. 調整 `solveRow()` 內部的程式碼，讓它解決關卡中更大的部分。
3. 呼叫 `solveRow()` 以及其他指令來通過關卡。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/e1b2e600-7b80-4f49-7c5f-fa46213e0b00/public)

## 講解

這關的主要目標是學習如何使用函數來簡化和組織你的程式碼。這種逐步拆分複雜任務的方法不僅可以使程式碼更容易閱讀和理解，還可以使程式碼更簡潔且易於維護。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func collectGemTurnAround() {
    moveForward()
    moveForward()
    collectGem()
    turnLeft()
    turnLeft()
    moveForward()
    moveForward()
}
func solveRow() {
    collectGemTurnAround()
    collectGemTurnAround()
}
solveRow()
turnRight()
moveForward()
turnLeft()
solveRow()
turnRight()
moveForward()
turnLeft()
solveRow()
```

## 後記

很好，你已經成功地利用函數將一個複雜的問題分解成多個小的問題。這是一個很好的開發習慣，可以讓你的程式碼更易於閱讀和維護。未來，在你編寫更複雜的程式碼時，不要忘記這個簡單而有用的開發技巧。

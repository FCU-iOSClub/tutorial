# 世界的角落

挑戰：修改兩個傳送門的狀態來通過關卡。

## 簡介

在這項挑戰中，關卡世界裡有很多寶石和開關，還有好幾個傳送門可以通過。這表示通關的方式有很多種。

在編寫程式碼時，請試著在腦海中思考不同的解決方法並找出最有效率的一種。編寫有效率的程式碼可讓程式更快速執行，進而讓使用者得到愉快的體驗並增進電池的續航力。

請使用 `greenPortal` 和 `orangePortal` 來存取傳送門。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/f310438a-4cc1-4092-27ad-2e52f5385700/public)
<!-- TODO:圖放錯ㄌ -->

## 講解

花一分鐘來檢視關卡，看看你目前學習的哪些技巧對通過關卡最有用處。解決方法有很多種，試試看你想到的其中一種方法吧！

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func turnAround() {
    turnLeft()
    turnLeft()
}
func checkSquare() {
    if isOnGem {
        collectGem()
    } else if isOnClosedSwitch {
        toggleSwitch()
    }
}
func collectOrToggle() {
    moveForward()
    checkSquare()
    turnAround()
}
func collectOrToggleThenTurnRight() {
    collectOrToggle()
    moveForward()
    turnRight()
}
func collectOrToggleThenTurnLeft() {
    collectOrToggle()
    moveForward()
    turnLeft()
}
turnLeft()
moveForward()
moveForward()
greenPortal.isActive = false
for i in 1...3 {
    collectOrToggleThenTurnRight()
}
collectOrToggle()
greenPortal.isActive = true
moveForward()
greenPortal.isActive = false
collectOrToggleThenTurnLeft()
collectOrToggleThenTurnLeft()
moveForward()
moveForward()
orangePortal.isActive = false
moveForward()
for i in 1...3 {
    collectOrToggleThenTurnRight()
}
collectOrToggle()
orangePortal.isActive = true
moveForward()
orangePortal.isActive = false
turnLeft()
collectOrToggleThenTurnRight()
collectOrToggle()
```

## 後記

你剛剛通過了一個困難的挑戰！透過檢驗問題和選擇要使用的技巧，你持續地訓練大腦分辦如何解決一系列的問題。隨著經驗的累積，你就可以更快速且有效率地解決新問題了。

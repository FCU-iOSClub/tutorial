# 橫掃四方

挑戰：練習發現模式、分解、函數和 for 迥圈。

## 簡介

不要被這項挑戰嚇倒；你一定做得到！首先集中精力解決離你角色最近的一組寶石和傅洪門。你能想出收集寶石並移動到下一個位置的模式嗎？

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/f08228ec-aa90-475c-390a-f2e4bc374200/public)

## 講解

注意每四顆寶石如何構成一組完全相同的佈局。針對其中一組編寫程式碼，以便套用到其他各組。

嘗試解決四組中的其中一組，然後讓你的角色穿過傳送門，並且加入迥圈來重複這組動作。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func turnAround() {
    turnRight()
    turnRight()
}
func collectFour() {
    collectGem()
    moveForward()
    collectGem()
    turnAround()
    moveForward()
    turnRight()
    moveForward()
    collectGem()
    turnAround()
    moveForward()
    moveForward()
    collectGem()
}
moveForward()
for i in 1...3 {
    collectFour()
    moveForward()
    moveForward()
}
collectFour()
```

## 後記

真是厲害！你找到了目前最困難問題的解決方法！猜猜看接下來要做什麼？你應該已經準備好學習下一個主要技巧：條件碼。

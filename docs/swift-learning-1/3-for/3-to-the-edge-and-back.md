# 走到邊緣再返回

挑戰：使用一個 for 迴圈來重複輪轉模式。

## 簡介

在這項挑戰中，同學們將練習如何尋找重複模式。你必須打開四個開關，方法是從中心點分別移動到每個開關。

通過這一關的第一步是，找出讓角色打開第一個開關並回到中心點所需的指令序列。這是重複執行的序列，因此請將程式碼放入大括號內。

你能看出哪一個額外的重複指令可以讓重複模式用於所有開關嗎？

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/9e8b94b8-1930-47eb-b7a2-fb9cdf249800/public)

## 講解

首先，在程式碼中加入 for 迴圈。

通過此關卡有兩種可能的方法。一種是每次執行迥圈時，讓角色從中央出發，然後再走回中央位置。另一種是讓角色走到正方形的外圈，然後使用迥圈繞著每個角落走。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
for i in 1...4 {
    moveForward()
    moveForward()
    toggleSwitch()
    turnRight()
    turnRight()
    moveForward()
    moveForward()
    turnLeft()
}
```

## 後記

做得很好！你已經掌握了這個技巧。

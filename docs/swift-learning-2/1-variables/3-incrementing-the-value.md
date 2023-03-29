# 讓變數變大吧

目標:遞增變數來追蹤已蒐集的寶石數量

## 簡介

在上一項挑戰中，如果你不知道關卡中的寶石數量，則不能設定1、2或3
這樣確切的值。你需要比較其現有的值來增加變數的值。這種程式設計模式
稱為遞增值

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/58b2fcf6-f8ec-4b8d-83a3-09ea7d69a400/public)

## 講解

這個關卡中會在你每次執行時產生隨機數量的寶石。你無法知道寶石是否位於
特定位置，因此需要檢查每個磚塊。只要發現寶石，你就需要收集寶石並將`gemCounter`的值遞增`1`

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
var gemCounter = 0
while !isBlocked {
    while !isBlocked {
        if isOnGem {
            collectGem()
            gemCounter = gemCounter + 1
        }
        moveForward()
    }
    turnRight()
}
```

## 後記

恭喜你完成了這次挑戰，繼續保持這股熱情往下一關吧!!

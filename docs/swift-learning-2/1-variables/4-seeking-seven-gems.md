# 尋找七顆寶石

目標:收集剛好七顆寶石

## 簡介

你已經學習使用變數在需要時遞增值，進而紀錄一個變化的值。在新的這關
中，你將使用此一知識來收集剛好七顆寶石。寶石出現的位置和次數都是隨
機的。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/dbbe4e99-62a1-43cf-a663-0dd4ab87c300/public)

## 講解

若要通關，你需要使用一個`while`迴圈，其中包含當你收集到七顆寶石
後回傳`false`的布林值條件。你將使用比較運算子(`<`)將`gemCounter`的
值與`Int`值7進行比較

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
var gemCounter = 0
while gemCounter < 7 {
    if isOnGem {
        collectGem()
        gemCounter = gemCounter + 1
    }
    if isBlocked {
        turnRight()
        turnRight()
    }
    moveForward()
} 
```

## 後記

太棒了!你已經學會如何利用迴圈與變數的應用，緊接著繼續學習更多知識吧

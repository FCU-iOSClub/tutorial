# 迴圈跳躍者

挑戰：辨識跳躍通過傅送門的重複模式。

## 簡介

在這個關卡中，有一種簡單的模式可以應用到每顆寶石上。思考如何收集第一顆寶石，然後看看相同的模式是否適用於所有寶石。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/2232e38d-ed5b-492e-1a59-586172c74a00/public)

## 講解

先查看關卡，第一眼可能比較難看出模式。建立迴圈前，先嘗試解決關卡的其中一部分。

你需要向前走，左轉，向前走兩步，然後右轉。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
for i in 1...5 {
    moveForward()
    turnLeft()
    moveForward()
    moveForward()
    collectGem()
    turnRight()
} 
```

## 後記

非常好！回想一下之前學過的技巧：指令、函數和 for 迴圈。在程式設計者的成長之路上，將會繼續使用所有這些技巧。

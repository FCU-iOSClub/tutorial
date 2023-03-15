# 結合世界

目標：加入新的磚塊來連接两個世界。

## 簡介

在此之前，關卡世界都是已經定義好的空間，現在你可以開始對這個世界進行更動。

這個關卡中的開關位於無法到達的區域，因此你需要加入磚塊，將這關的兩個部分連接起來。

1. 首先，建立一個 Block 類型的實例。
2. 接著，使用點記法存取 world 實例並呼叫 place 方法。
3. 將引數傳入 place 方法中。在 item 參數中使用 Block 實例，並將一組座標用於 atColumn 和 row 參數。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/c8cbcf50-1823-49e4-cb43-8b6a3ba32200/public)

## 講解

試試看在座標 (1,1) 處放置磚塊。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let block1 = Block()
world.place(block1, atColumn: 3, row: 3)
while !isOnClosedSwitch {
    moveForward()
    if isBlocked {
        turnLeft()
        if isBlocked {
            turnRight()
            turnRight()
        }
    }
}
toggleSwitch()
```

## 後記

你現在有能力可以替世界添加磚塊了。是不是很棒呢？繼續往下學習，你會學到使用程式碼操控關卡世界的新方法。

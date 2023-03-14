# 連接並解決

挑戰：加入磚塊來填滿所有缺口。

## 簡介

在這項挑戰中，要練習調整關卡世界。你需要加入多個磚塊來到達寶石處。你可以將一個磚塊放在另一個磚塊上，藉此來堆疊碼塊。

請務必使用迥圈，並將你的程式碼分解成函數，這樣可避免多次重寫相同行數的程式碼。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/032018b0-2e37-4843-81a5-24074ef2ad00/public)

## 講解

你需要建立多個 Block 類型的實例，並將它們放置在能讓你成功通關的位置。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let block1 = Block()
let block2 = Block()
let block3 = Block()
let block4 = Block()
let block5 = Block()
world.place(block1, atColumn: 2, row: 2)
world.place(block2, atColumn: 2, row: 2)
world.place(block3, atColumn: 4, row: 2)
world.place(block4, atColumn: 6, row: 2)
world.place(block5, atColumn: 6, row: 2)
func crossBridge() {
    turnRight()
    move(distance: 4)
    collectGem()
    turnLeft()
    turnLeft()
    move(distance: 4)
    turnRight()
}
for i in 1...3 {
    move(distance: 2)
    toggleSwitch()
    crossBridge()
}
```

## 後記

你已開始使用有效的新方法來組合你學習到的所有程式設計技巧了。接著，你將瞭解如何放置另一種項目「傅送門」。

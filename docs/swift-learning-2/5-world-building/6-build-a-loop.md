# 建立迴圈

挑戰：建構你的世界並收集數量隨機的寶石，以常數
totalGems 表示。

## 簡介

在這個關卡中，你每次執行程式碼都會產生隨機數量的寶石。你的目標是調整關卡世界，以便在其中有效率地穿梭行走，直到收集完所有寶石。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/ae7a952f-38a3-4d0e-9802-59846545b600/public)

## 講解

首先，你需要建構關卡世界的一部分，才能夠到達產生了寶石的位置。

寶石的數量由常數 totalGems 中儲存的值來決定。記錄已收集的寶石數量，這樣才能知道何時要停止執行程式碼。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let totalGems = randomNumberOfGems
var gemCounter = 0
world.place(Block(), atColumn: 0, row: 2)
world.place(Block(), atColumn: 3, row: 3)
let expert = Expert()
world.place(expert, facing: east, atColumn: 2, row: 3)
while gemCounter < totalGems {
    if expert.isOnGem {
        expert.collectGem()
        gemCounter = gemCounter + 1
    }
    if expert.isBlocked {
        expert.turnRight()
        if expert.isBlocked {
            expert.turnRight()
            if expert.isBlocked {
                expert.turnRight()
            }
        }
    }
    expert.moveForward()
}
```

## 後記

現在應該對關卡世界的每個部分進行修改了。準備好了嗎？

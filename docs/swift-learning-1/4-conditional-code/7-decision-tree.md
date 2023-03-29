# 決定樹

目標：測試關卡世界的狀態來更改路線。

## 簡介

在這最後一項挑戰中，你需要沿著中央的平臺收集寶石和切換開關，但中途出現了幾條岔路。
你可以使用條件碼來檢測你的角色是否位於寶石或關開的開關處，並且，如果你的角色所處的位置類型不同，則採取不同的行動。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/15ae4d78-049a-4819-fecd-a3f7a1b49400/public)

## 講解

從地圖上可以看到兩個規律

1. 在寶石的磚塊上，需要向右走收集另一顆寶石。
2. 在關閉的開關上，需要向左走收集寶石。

於是設定一個函數 `solveRightSide()` 來收集右手邊的寶石。並且透過 `if else` 來判斷目前要往左手邊走還是右手邊。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func solveRightSide() {
    collectGem()
    turnRight()
    moveForward()
    moveForward()
    moveForward()
    turnLeft()
    moveForward()
    collectGem()
    turnLeft()
    turnLeft()
    moveForward()
    turnRight()
    moveForward()
    moveForward()
    moveForward()
    turnRight()
}
for i in 1...5 {
    moveForward()
    if isOnGem {
        solveRightSide()
    } else if isOnClosedSwitch {
        toggleSwitch()
        turnLeft()
        moveForward()
        collectGem()
        turnLeft()
        turnLeft()
        moveForward()
        turnLeft()
    }
}
```

## 後記

恭喜你完成條件碼！
你的程式設計能力日益強大。現在你可以使用 if 語句在特定情況下執行特定的程式碼區塊了。下一步，你將學習邏輯運算子，這種符號會影響條件碼執行的方式。

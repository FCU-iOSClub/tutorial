# TODO

使用 AND 運算子來結合兩個條件，並在兩者皆為真時調整你的路徑。

## 簡介

邏輯 AND 運算子(&&)會結合兩個布林值條件，並且只有在兩者皆為真時才會執行程式碼。例如：在下列程式碼中，`isBlocked` 和 `isOnclosedswitch` 都必須為真。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/e4350837-06e9-4954-9264-864d91e95b00/public)

## 講解

在本題關卡中，我們使用 AND 運算子結合了兩個條件 isOnGem 和 isBlockedLeft。只有當機器人正好在寶石上且左邊被阻擋時，才會執行 if 語句塊中的程式碼。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
for i in 1 ... 7 {
    moveForward()
    if isOnGem && isBlockedLeft {
        collectGem()
        turnRight()
        moveForward()
        moveForward()
        toggleSwitch()
        turnLeft()
        turnLeft()
        moveForward()
        moveForward()
        turnRight()
    } else if isOnGem {
        collectGem()
    }
}
```

## 後記

使用 AND 運算子來結合兩個條件，進而控制 Byte 的行為。 AND 運算子是一個重要的邏輯運算符，可以讓我們更加靈活地控制程式的執行流程。綜合應用邏輯運算符可以讓我們編寫更複雜的程式，實現更多樣化的功能。通過不斷的練習和實踐，相信大家都可以熟練掌握這些技能，寫出更高效、更優雅的程式碼，加油！

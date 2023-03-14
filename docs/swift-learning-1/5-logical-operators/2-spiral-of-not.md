# TODO

挑戰：使用 NOT 運算子來在受阻時左轉。

## 簡介

就像上一個練習一樣，這個挑戰中的關卡世界在你每次執行的時候都會有點不一樣。試著理解怎麼使用邏輯 NOT 運算 `!` 來通關。

> 條件 `isBlocked` 提供了一個非真即偽的布林值。

> 如果你無法朝目前的方向往前走一步，`isBlocked` 則為真。如果你可以向前走，`isBlocked` 即為偽

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/4ea0f9ed-2924-416f-8455-c961501ddb00/public)

## 講解

在這個挑戰中，你可以使用 NOT 運算符來讓 Byte 在遇到障礙物時改變方向，繼續前進，直到到達目標區域。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
for i in 1...16 {
    if !isBlocked {
        moveForward()
    } else {
        turnLeft()
    }
}
toggleSwitch()
```

## 後記

如果你很輕鬆的完成 NOT 螺旋這個挑戰，代表你已經掌握簡單的邏輯運算子運用了，接下去挑戰其他更有挑戰性的關卡吧！

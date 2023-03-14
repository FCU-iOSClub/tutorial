# TODO

目標：使用 NOT 運算子，在磚塊上沒有寶石時調整角色的路線。

## 簡介

邏輯 NOT 運算子`！`將布林值更改為其相反的值，即反轉值。

例如，如果條件 `isBlocked` （受阻）為偽，則 `!isBlocked`（不受阻）為真。

執行幾次這一關，看看有什麼雙化。注意這一關中始終會有四顆寶石，但有一顆位於階梯的底端。當上方平臺沒有寶石時，會有階梯從磚塊處延伸出來。

我們先用 `!` 符號來判斷角色是不是在寶石上，如果是，我們就收集這顆寶石，如果不是，我們就去尋找階梯盡頭的寶石。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/4d757c53-d4a7-4fb3-3a86-9ae1f21d4500/public)

## 講解

做的好！現在你已經開始會使用邏輯 NOT 運算子反轉布林值了。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
for i in 1...4 {
    moveForward()
    if !isOnGem {
        turnLeft()
        moveForward()
        moveForward()
        collectGem()
        turnLeft()
        turnLeft()
        moveForward()
        moveForward()
        turnLeft()
    } else {
        collectGem()
    }
}
```

## 後記

當你通過學習使用 NOT 運算子，你已經跨越了學習程式設計的一個重要障礙。這是一個很好的開始，它為你接下來的學習程式設計打下了堅實的基礎。使用 NOT 運算子可以讓你更好地理解邏輯運算和條件控制，這是編程中非常重要的基礎概念唷。

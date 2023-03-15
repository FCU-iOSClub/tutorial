# TODO

目標：使用 OR 運算子，在兩個條件裡有一個成立時，調整角色的路線。

## 簡介

最後一個邏輯運算子是邏輯 OR 運算子 (||)，它結合兩個布林值條件，且在至少一個為 true 時執行程式碼。例如，在下方的程式碼中，`isOnGem` 或 `isBlockedLeft`
必須為 `true` 才能執行 `moveForward()`。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/d00ee4bb-26d2-48bb-0194-47dfaa9eec00/public)

## 講解

仔細觀察地圖的邏輯後會發現：如果兩個條件均為偽，則程式碼不會執行。如果其中一個或者二者均為真，則程式碼執行。

1. 使用1運算子來檢查其中一個條件是否為真。提示： 
   * 你可能前方受阻或左邊受阻。
2. 如果其中一個為真，則右轉並向前走。
3. 如果二者均為偽，則向前走。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
for i in 1...12 {
    if isBlocked || isBlockedLeft {
        turnRight()
        moveForward()
    } else {
        moveForward()
    }
}
collectGem()
```

## 後記

仔細觀察關卡所需條件後再進行程式的編寫可以讓你在程式設計更有效率同時也更順暢，有時候關卡比較複雜不要灰心，多觀察一下再下手，你一定可以的！

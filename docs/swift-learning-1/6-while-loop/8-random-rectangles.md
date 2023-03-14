# 隨機矩形

挑戰：使用嵌套迴圈和條件在不斷變化的世界中走動。

## 簡介

在這項挑戰中，執行幾次這一關，看看關卡世界如何在保持形狀不變的同時改變其大小。

與上一個練習中一樣，你可以使用嵌套迴圈來建立各種關卡世界大小都適用的解決方案。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/eb0f00fe-1067-4e6c-c932-38a31bf39300/public)

## 講解

你可以使用嵌套迴圈來建立一個網格，網格的大小會根據每個關卡的大小而變化。然後，你可以使用條件來控制你的角色移動。在每個迴圈中，你需要檢查你的角色是否在邊界內，如果是，你的角色就需要轉向。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
while !isBlocked {
    while !isBlocked {
        moveForward()
    }
    turnRight()
}
toggleSwitch()
```

## 後記

希望你在這個關卡中有所收穫，並能夠將所學的知識應用到實際的編程中。不斷練習和嘗試新的技巧，相信你一定可以成為一名優秀的程式設計師！

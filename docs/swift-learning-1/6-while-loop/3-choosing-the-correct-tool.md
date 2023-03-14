# 選擇正確的工具

目標：選取最合適的迴圈來收集所有寶石。

## 簡介

這一關有六顆寶石，你的角色可以遵循一種簡單的模式。最佳的通關方式是使用迴圈，但用哪一種呢？你可以使用 while 迴圈，使其在不受阻時保持走動。或者可以使用 for 迴圈來重複特定次數的模式，因為你已經知道寶石的數量。

有時候，決定如何解決一個程式設計問題只是個人傾向的選擇而已。當程式設計者面臨這種選擇時，他們會根據解決方案的簡潔性或重複利用的可能性來決定。

1. 識別從一顆寶石走到下一顆寶石的模式。
2. 選取一種迴圈並用它來通關。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/c37a2d77-bc68-49ba-9895-00c04261d600/public)

## 講解

有時候，程式設計師會根據簡潔性或個人喜好選擇使用 while 迴圈或 for 迴圈。在這方面，對你來說，哪一種方式比較容易理解呢？

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func turnAndCollectGem() {
    moveForward()
    turnLeft()
    moveForward()
    collectGem()
    turnRight()
}
while !isBlocked {
    turnAndCollectGem()
}
```

## 後記

通過這個練習，你已經學會了如何選擇最適合的迴圈來解決問題。在 Swift 中，for 和 while 迴圈是最常用的迴圈結構，可以幫助你處理大量數據和執行重複任務。在解決問題時，選擇最適合的迴圈結構可以使你的程式更加高效和可讀。熟悉迴圈和控制流程是成為一名優秀 Swift 程式設計師的關鍵。

# 尋寶

挑戰：分解模式並建立你自己的函數

## 簡介

在這最後一項挑戰中，先找出一個小的指令模式，並且建立一個函數來呼叫這些指令。使用該函數來開始通過部分關卡。

範例：

```swift
func moveThenToggle(){
    moveForward()
    moveForward()
    toggleSwitch()
}
```

當你發現關卡中更為複雜的部分時，定義一個新函數，讓它使用第一個函數中的指令。然後使用這兩個函數來通關。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/19c480ab-dee6-4114-abae-2489bd582900/public)

## 講解

這個挑戰比較具有挑戰性，如果你覺得困難可以先跳過，挑戰後面的關卡。等你更熟悉程式設計後，再回來挑戰！

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func moveThenToggle() {
    moveForward()
    moveForward()
    toggleSwitch()
}
func toggleThenReturn() {
    moveThenToggle()
    turnLeft()
    turnLeft()
    moveForward()
    moveForward()
}
toggleThenReturn()
toggleThenReturn()
turnRight()
moveThenToggle()
toggleThenReturn()
moveForward()
moveForward()
moveThenToggle()
moveThenToggle()
```

## 後記

在這個挑戰中，我們學習了如何使用函數來處理風格類似的指令。定義一個函數，可以大大簡化整個流程，也讓程式碼看起來更舒服。所以，如果你完成了這關挑戰，代表你已經掌握了基礎的函數應用。

另外，你可能已經發現，如果有些指令需要重複執行，我們每次都要重複的寫一長串，程式會變得非常冗長。現在請繼續前往下一章學習「For 迴圈」，這是學習程式設計中非常重要的一章，也會遇到許多有趣的關卡！

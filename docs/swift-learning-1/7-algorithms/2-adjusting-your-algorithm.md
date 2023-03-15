# 調整你的演算法

目標：調整演算法來繞過額外的障礙。

## 簡介

這一關與上一關類似，但牆的周圍增加了其他障礙，導致你的右手規則演算法無法正常運行。
在某些情況下，你的右邊受阻，但你也無法前行，因為前方同樣受阻。

若要解決問題，你需要改善演算法。
上方的圖像顯示了你的角色將遇到的三種不同情況，同時箭頭提供了如何回應每種情況的建議。
你能修改navigateAroundwall() 來處理每種情況嗎？

1. 使用虛擬碼，思考你的角色在上面三種情況中應當如何移動。
2. 根據你的虛擬碼，調整下方現有的程式碼，然後執行看看會發生什麼。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/3d5ccf10-6e7f-4064-c3f8-cdfc5c798c00/public)

## 講解

在此，我們定義了一個名為 navigateAroundWall() 的函數。
此函數會檢查右側和前方是否有障礙物。如果右側和前方都有障礙物，則向左轉。如果右側有障礙物但前方沒有障礙物，則向前移動。
如果右側沒有障礙物，則向右轉並向前移動。

緊接著一個 while 迴圈，只要玩家沒有在封閉的開關上，就會一直運行。
在迴圈內，我們調用了之前定義的 navigateAroundWall() 函數。
如果玩家在寶石上，那麼程式碼會執行 collectGem() 函數，收集寶石。

最後，程式碼會切換開關。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func navigateAroundWall() {
    if isBlockedRight && isBlocked {
        turnLeft()
    } else if isBlockedRight {
        moveForward()
    } else {
        turnRight()
        moveForward()
    }
}
while !isOnClosedSwitch {
    navigateAroundWall()
    if isOnGem {
        collectGem()
    }
}
toggleSwitch()
```

## 後記

這段程式碼示範了如何使用 Swift Playground 中的函數和迴圈來完成一些簡單的動作，並且可以用來幫助學生理解 Swift 編程的基本概念。

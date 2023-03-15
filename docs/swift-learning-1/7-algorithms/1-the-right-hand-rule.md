# 右手規則

目標：使用「右手規則」演算法來繞牆走動。

## 簡介

執行本關卡，注意角色如何在第一顆寶石處停下。
這裡使用的演算法遵循右手規則來繞牆走動。
若要通關，你需要改善演算法，但首先請嘗試使用虛擬碼來規劃行動。
虛擬碼看起來與 Swift 程式碼有點類似，但它採用的是人類易懂的措辭和結構。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/46173b8e-ec4f-402a-0bc1-0b26f0ae4600/public)

## 講解

在此，我們定義了一個名為 navigateAroundWall()的函數。此函數檢查是否有牆壁在右側。
如果右側有牆壁，則向前移動。如果右側沒有牆壁，則向右轉並向前移動。

緊接著一個 while 迴圈，只要玩家沒有在封閉的開關上，就會一直運行。在迴圈內，我們調用了之前定義的 navigateAroundWall() 函數。
如果玩家在寶石上，那麼程式碼會執行 collectGem() 函數，收集寶石。然後，玩家會向左轉兩次。

最後，程式碼會切換開關。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func navigateAroundWall() {
    if isBlockedRight {
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
        turnLeft()
        turnLeft()
    }
}
toggleSwitch() 
```

## 後記

這段程式碼示範了如何使用 Swift Playground 中的函數和迴圈來完成一些簡單的動作，並且可以用來幫助學生理解 Swift 編程的基本概念。

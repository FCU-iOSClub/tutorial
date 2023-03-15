# 征服迷宮

目標：使用右手規則來走出迷宮。

## 簡介

遵循右手規則的演算法能夠有效通過簡單的關卡，但你知不知道，用它來穿行類似迷宮這樣更加複雜的路線也可行。

在這一關中，請先在腦海中思考穿過迷宮的途徑。如果始終遵循右手規則，你最終會到達最後一顆寶石處。
若要破解迷宮，請調整你上一頁的演算法來導航到寶石處並收集它。

1. 用剪貼的方式，根據上一頁的程式碼開始設計，或者如果想挑戰一下自己，也可以從頭開始程式設計。
2. 調整程式碼，使角色遵循右手規則穿過迷宮，直至到達寶石處。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/a52ea4ff-b1da-4946-3ba9-8129c2727a00/public)

## 講解

在此，我們定義了一個名為 navigateAroundWall() 的函數。
此函數會檢查右側和前方是否有障礙物。如果右側和前方都有障礙物，則向左轉。
如果右側有障礙物但前方沒有障礙物，則向前移動。
如果右側沒有障礙物，則向右轉並向前移動。

緊接著一個 while 迴圈，只要玩家沒有在寶石上，就會一直運行。
在迴圈內，我們調用了之前定義的 navigateAroundWall() 函數。

當迴圈停止運行時，表示玩家已經到達了寶石位置。因此，我們執行 collectGem() 函數來收集寶石。

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
while !isOnGem {
    navigateAroundWall()
}
collectGem()
```

## 後記

這段程式碼示範了如何使用 Swift Playground 中的函數和迴圈來自動尋找寶石並收集它。
這個例子展示了如何讓玩家在遊戲中完成特定的任務，並且可以用來幫助學生理解 Swift 編程的基本概念。

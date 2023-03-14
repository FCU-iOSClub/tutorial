# 遍佈隨機寶石

挑戰：收集數量隨機決定的寶石，以 totalGems 表示。

## 簡介

在這項挑戰中，寶石出現的位置和數量都是隨機的。你需要編寫一個演算法，讓角色在關卡世界中有效率地持續走動，收集任何出現的寶石。

讓角色有效率地走動的同時，思考如何能使程式碼更加簡潔。嘗試將動作分解成可重複使用的函數，這樣所需的程式碼行數就會減少。這稱為分解程式碼，這不僅對於函數的重複使用大有幫助，而且能讓任何查看程式碼的人容易理解程式碼的內容。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/e4a47d56-fe70-4326-d600-f21bb13af200/public)

## 講解

宣告一個變數來追蹤你收集了多少顆寶石，並與 totalGems 常數做比較，以決定何時停止收集。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let totalGems = randomNumberOfGems
var gemCounter = 0
bluePortal.isActive = false
pinkPortal.isActive = false
while gemCounter < totalGems {
    if isOnGem {
        collectGem()
        gemCounter = gemCounter + 1
    }
    moveForward()
    if isBlocked {
        turnLeft()
        turnLeft()
        if bluePortal.isActive == true {
            bluePortal.isActive = false
            pinkPortal.isActive = false
        } else if bluePortal.isActive == false {
            bluePortal.isActive = true
            pinkPortal.isActive = true
        }
    }
}

```

## 後記

你的程式設計技巧進步神速。現在應該學習一組新的技巧了。準備好開始了嗎？

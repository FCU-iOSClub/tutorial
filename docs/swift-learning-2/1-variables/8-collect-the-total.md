# 收集總數

挑戰: 收集數量隨機決定的寶石,以`totalGems` 表示。

## 簡介

這項挑戰中提供了一個從1到12中隨機生成的常數,即`totalGems`,使用
這個常數來編寫程式碼,收集 `totalGems` 中定義的寶石數量,並在達到此
數量後停止。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/cd76dbd6-d0de-485a-7b20-923b9c9c3500/public)

## 講解

你需要先獲得隨機數值的totalGems，並且利用while迴圈判斷當收集到的寶石小於全部寶石時
就繼續執行下去，而執行的動作有當在寶石上時就收集寶石，如果遇到障礙時先右轉再判定是否
碰到障礙，如果還是碰到障礙則左轉兩次，那如果還是碰到障礙就在左轉一次。如果沒遇到寶石
或障礙就繼續前進吧。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let totalGems = randomNumberOfGems
var gemCounter = 0
while gemCounter < totalGems {
    if isOnGem {
        collectGem()
        gemCounter = gemCounter + 1
    }
    if isBlocked {
        turnRight()
        if isBlocked {
            turnLeft()
            turnLeft()
            if isBlocked {
                turnLeft()
            }
        }
    }
    moveForward()
}
```

## 後記

恭喜你!!!完成了變數關卡!!!請繼續加油喔~~

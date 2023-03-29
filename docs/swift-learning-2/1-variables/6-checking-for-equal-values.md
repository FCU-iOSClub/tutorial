# 檢查相等值

目標:收集與開關數量相等的寶石

## 簡介

在這個關卡中,你將使用稱為 `switchCounter` 的常數來收集與開關數量相
同的寶石。常數與變數相似,都是用來儲存值且被命名的容器。但是,常數
的值在程式執行時不能更改。


![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/c3cb4d11-d4e2-46d1-9702-824359019d00/public)

## 講解

常數會使用 `let` 而非 `var` 來宣告,並且用於你知道值不會更改的情況中。
宣告常數
let numberOfTries = 3
為了通過此關卡,你將編寫讓計算寶石數量的變數的值與 `switchCounter`
(儲存關卡中隨機顯示的開關數量的常數) 進行比較的條件碼。若要比較這
兩個值,請使用比較運算子,例如`<`、`>`、`=`或`!=`
1 宣告一個變數來追蹤已收集的寶石數量。
2 將計算寶石數量的變數值與 `switchCounter` 相比較,以決定何時停止
收集寶石。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let switchCounter = numberOfSwitches
var gemCounter = 0
while gemCounter < switchCounter {
    if isOnGem {
        collectGem()
        gemCounter = gemCounter + 1
    }
    if isBlocked {
        turnRight()
    }
    moveForward()
}
```

## 後記

恭喜你！學會了如何使用Let和var應用於程式當中，繼續加油喔~

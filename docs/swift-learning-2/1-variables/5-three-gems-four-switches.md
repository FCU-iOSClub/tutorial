# 三顆寶石，四個開關

挑戰:收集剛好三顆寶石並打開四個開關。

## 簡介

在這項挑戰中，為收集到正確數量的寶石並打開正確數量的開關，你分別需
要兩個變數。在你的角色處理寶石和開關時，遞增正確的變數，讓角色在適
當的時間停止動作。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/1b411196-e4da-4a39-aed1-6aa7d4130700/public)

## 講解

首先為寶石數量宣告一個變數，然後在為開關數量宣告另一個變數。根據以
下的指示來為你的變數命名。
為變數命名
使用駝峰式大小寫:開頭第一個單詞使用小寫字母，然後將每個新單詞的首
個字母大寫。
使用描述性名稱:為變數命名時說明他所儲存的內容，例如
`numberOfCats`。

收集一顆寶石或打開一個開關將相應變數遞增`1`。使用下列其中一個比
較運算子，在`if`語句或`while`迴圈中建立條件，告訴角色何時停止。
更多比較運算子
小於運算子 : 如果`a`小於`b`，則(`a < b`)傳回`true`。
大於運算子 : 如果`a`大於`b`，則(`a > b`)傳回`true`。
等於運算子 : 如果`a`等於`b`，則(`a == b`)傳回`true`。
不等於運算子 : 如果`a`不等於`b`，則(`a != b`)傳回`true`。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
var gemCounter = 0
var switchCounter = 0
while gemCounter != 3 || switchCounter != 4 {
    if gemCounter != 3 && isOnGem {
        collectGem()
        gemCounter = gemCounter + 1
    } else if switchCounter != 4 && isOnClosedSwitch {
        toggleSwitch()
        switchCounter = switchCounter + 1
    }
    if isBlocked {
        turnRight()
        if isBlocked {
            turnLeft()
            turnLeft()
        }
    }
    moveForward()
} 
```

## 後記

太棒了!! 你學會如何利用迴圈以及比較運算子的應用，繼續加油喔~~

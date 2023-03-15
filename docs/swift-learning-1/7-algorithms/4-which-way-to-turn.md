# 左轉還是右轉

練習：寫下自己的演算法來通關。

## 簡介

目前為止你已經改善了不少演算法；是時候來練習學到的東西，並從頭開始編寫你自己的演算法。

若要完成這個關卡，你需要依照路徑前往每個開關處，決定要左轉還是右轉。嘗試在關卡中找出模式，以推敲出該轉哪個方向。

1. 在腦海中走過虛擬碼，思考如何切換六個開關並得到寶石。
2. 寫出你的程式碼，測試演算法並在需要時進行調整。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/e3acd94f-6c05-44df-7dd4-1d0d630ad200/public)

## 講解

最外層是一個 while 迴圈，在玩家沒有到達寶石或開關時會一直運行。在迴圈內，玩家會不斷向前移動以尋找寶石和開關。

當玩家到達開關時，這個 if...else if 陳述式會檢查左側和前方是否有障礙物。

如果左側和前方都有障礙物，玩家會切換開關並向左轉。如果只有前方有障礙物，玩家會切換開關並向右轉。

當玩家到達寶石時，迴圈停止運行並執行 collectGem() 函數以收集寶石。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
while !isOnGem {
    while !isOnClosedSwitch && !isOnGem {
        moveForward()
    }
    if isOnClosedSwitch && isBlocked {
        toggleSwitch()
        turnLeft()
    } else if isOnClosedSwitch {
        toggleSwitch()
        turnRight()
    }
}
collectGem()
```

## 後記

這段程式碼展示了如何使用 Swift Playground 中的迴圈和條件陳述式來自動尋找寶石和開關，並且可以用來幫助學生理解 Swift 編程的基本概念。

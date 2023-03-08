# 嵌套模式

目標：從其他函數呼叫函數

## 簡介

到目前為止，你定義過的函數只呼叫了現有的指令，例如moveForward(）和collectcem(）。但還有別種方式！

函數 `turnAround()` 會引導你的角色轉身並面向相反的方向。你可以在另一個函數 `solvestair()` 中呼叫這個函數，並在你的程式碼中呼叫 `solvestair()` 來解決關卡中較大的區域。

這個將較大的問題分解成較小部分的過程稱為分解。

1. 定義 `solvestair()`（函數，在其內呼叫 turnAroundl)。
2. 呼叫 `solvestair()`（和你所需要的其他函數）。
3. 收集全部四顆寶石通過關卡。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/004ba2c0-61a2-4839-0652-6b971fb92900/public)

## 講解

在一個函數中，是可以呼叫其他的函數的，試著組合自己寫過的函數，讓程式更為簡潔。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func turnAround() {
    furnLeft()
    turnLeft()
}
func solveStair() {
    moveForward()
    collectGem()
    turnAround()
    moveForward()
    turnLeft()
}
solveStair()
solveStair()
solveStair()
solveStair()
```

## 後記

相信你已經更瞭解函數在程式設計中扮演的角色。在下一關中，我們將繼續瞭解更多的函數用法！

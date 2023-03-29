# 困在裡面

目標：運用條件、函數和迥圈來好好組織你的程式碼。

## 簡介

在這項挑戰中，你的角色被可能的寶石或開關位置組成的網格所包圍。開始動腦筋，想出如何走到正確的位置去收集寶石和打開開關。你需要用到函數、迥圈和條件。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/f07d6452-2d24-46eb-38e3-116b69995e00/public)

## 講解

設定一個函數 `checkSquare()` 來判斷是否在寶石或是開關上。接著在迷宮中，我們可以看出一個規律，檢查開關之後往前走一步，再次檢查開關之後向右轉，以此規律執行四次我們即可走完一整圈，於是我們設立另一個函數 `completeCorner()` 來解決此問題。最後用 for 迴圈執行重複動作。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func checkSquare() {
    if isOnGem {
        collectGem()
    } else if isOnClosedSwitch {
        toggleSwitch()
    }
}
func completeCorner() {
     checkSquare()
     moveForward()
     checkSquare()
     turnRight()
     moveForward()
}
moveForward()
turnRight()
for i in 1...4 {
     completeCorner()
}
```

## 後記

了不起！
你的解決方法真是不可思議。你進步得很快，學到了條件碼並將新技巧融入了函數和 for 迥圈中！

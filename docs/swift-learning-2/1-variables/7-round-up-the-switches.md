# 計算開關數量

挑戰: 切換與所收集寶石數量相同的開關。

## 簡介

在這項挑戰中,請在第二個平台上切換與第一個平台上所收集寶石數量相同
的開關。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/ce07548c-c477-46da-76ab-71abc6e6b100/public)

## 講解

指定快捷鍵:
使用複合指定值運算子為變數加入值的同時指定新的值。
下列兩行程式碼實際上做的事情完全相同,但使用 += 會更快!
範例
gemCounter = gemCounter + 1
gemCounter += 1
運用你掌握的變數、指定值和比較運算子知識來為這一關製作解決方法,請
記住,如果首次嘗試沒有得到解決方法也沒有關係!嘗試不同的步驟可讓你
在錯誤中學習,進而更深入地瞭解你所編寫的程式碼。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
var gemCounter = 0
var switchCounter = 0
while !isOnClosedSwitch {
    while !isBlocked {
        if isOnGem {
            collectGem()
            gemCounter = gemCounter + 1
        }
        moveForward()
    }
    turnRight()
}
while switchCounter < gemCounter {
    while !isBlocked {
        if isOnClosedSwitch && switchCounter < gemCounter {
            toggleSwitch()
            switchCounter = switchCounter + 1
        }
        moveForward()
    }
    turnRight()
}
```

## 後記

恭喜你學會了更進階的用法!!繼續加油喔~~

# 迴圈條件碼

目標：在迴圈中使用 `if語句` 來切換開關或收集寶石

## 簡介

這一關中有 12 個包含寶石、開關或傳送門的磚塊。如果磚塊上有寶石，則收集寶石。如果遇到關閉的開關，則將它打開。如果遇到傳送門，則前行即可。執行這一關時注意線框，它們會顯示可能出現的項目。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/f36e7229-842f-4e57-a927-f98fb1679f00/public)

## 講解

與其編寫一長串 `if語句` ，你可以將條件陳述式與迥圈相結合，在一個 `for 迴圈` 內部編寫你的邏輯。
另外，由於磚塊可能包含寶石、開關，或者二者皆無，這時則非常適合使用 `else if 區塊` 來檢查另一種條件。

1. 在下方的 `for` 迥圈中，在 `moveForward（）` 後加入一個 `if` 語句來檢查 `isOnGem` 或 `isOnClosedswitch` 。
2. 在你的 `if` 語句中加入一個 `else if` 區塊來檢查另一種條件。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
for i in 1...12 {
    moveForward()
    if isOnClosedSwitch {
        toggleSwitch()
    } else if isOnGem {
        collectGem()
    }
}
```

## 後記

做得很好！使用迥圈是一種讓程式碼可重複使用的方法。使用 if 語句也可讓程式碼更有適應性。即使迥圈的主體一次接著一次執行，但條件可以每次更改。

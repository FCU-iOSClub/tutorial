# 定義更聰明的函數

目標：使用函數、迴圈和條件來收集寶石或打開開關。

## 簡介

在這一關中，每隔一步可能遇到寶石、開關，也可能什麼都沒有。執行這一關時，線框會顯示項目可能出現的位置。若要通關，你可以編寫許多 `if語句` ，不過還有更好的辦法。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/a95f18a5-d1c5-4cec-602a-6cbc480f9100/public)

## 講解

首先，將整個關卡分解成基本的模式。主線路共有三條，每條上都有兩個位置會有寶石或開關。

1. 使用一個 `if` 語句定義 `collectOrToggle（）` （收集寶石或切換開關狀態）函數來檢查磚塊的內容。
2. 在函式定義下方，呼叫 `collectOrToggle（）` 及其他指令來通關。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func collectOrToggle() {
    moveForward()
    moveForward()
    if isOnGem {
        collectGem()
    } else if isOnClosedSwitch{
            toggleSwitch()
    }
}
collectOrToggle()
collectOrToggle()
turnLeft()
moveForward()
moveForward()
turnLeft()
collectOrToggle()
collectOrToggle()
turnRight()
moveForward()
turnRight()
collectOrToggle()
collectOrToggle()
```

## 後記

你真的懂了！使用包含 if 語句的函數是讓程式碼可重複使用且具適應性的另一種方法。你可以重複呼叫同一個函數，讓函數自動選擇正確的解決方法。

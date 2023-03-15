# 取個名字吧

目標:建立一個變數來追蹤已蒐集的寶石數量

## 簡介

在這關卡中，你需要紀錄收集的寶石數量。這個值一開始應該為 0；在角色收集第一顆寶石後，值應該更改為 1。

若要宣告(建立)一個變數，請使用 `var` 並為變數命名。然後使用指定值運算子 `=` 來設定變數初始值。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/7a06e127-5034-4f72-1364-a7854429d100/public)

## 講解

這題的目標是建立一個變數來記錄寶石的數量，我們只要在程式執行之前利用 `var` 空一個空白後打上自己想要的名稱就可以建立變數。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
var gemCounter = 0
moveForward()
moveForward()
collectGem()
gemCounter = 1
```

## 後記

真棒！你學會了如何建立變數了，請往下個關卡前進吧！

# 符合條件時往上爬

目標：使用 `if` 語句在你的角色位於寶石處時觸發一組指令。

## 簡介

恭喜！你已經學會如何在編寫條件碼時使用 `if語句` 和 `else if 區塊`。像 `isOnGem` 這樣的條件總是非真即偽。這稱為布林值。程式設計者經常結合條件碼使用布林值來告訴程式何時執行特定的程式碼區塊。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/66f4a768-1da5-4fd2-e551-d0c210c15100/public)

## 講解

1. 在下方的 `if` 語句中，使用布林條件 `isOnGem` ，並加入條件為真時所要執行的程式碼。
2. 修改或保留現有的 `else 區塊` 來在布林條件為偽時執行程式碼。
3. 必要時，調整 for 迥圈執行的次數。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
for i in 1...16 {
    if isOnGem {
        collectGem()
        turnLeft()
    } else {
        moveForward()
    }
}
```

## 後記

布林大師！
像 `isOnGem` 的條件稱為布林值：它總是非真即偽。在 if else 語句中，若布林值為真，即執行 if 語句；若布林值為偽，則執行 `else 區塊` 。

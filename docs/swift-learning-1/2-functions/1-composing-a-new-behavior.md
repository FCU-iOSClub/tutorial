# 組合新的動作

目標：使用指令組合來右轉。

## 簡介

你是否注意到沒有 `turnRight()` 這個指令？如果你的角色需要右轉才能到達寶石處，應該怎麼做？

有時為了解決程式設計的問題，你需要組合現有的指令來建立新的動作。這個過程稱為組合。

1. 動動腦筋，如何才能只用先前使用過的指令來右轉、
2. 使用組合來讓你的角色在需要時右轉。
3. 輸入指令來收集寶石。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/102adf40-b3ff-45f2-1c33-451b5d54c700/public)

## 講解

試著組合指令來右轉。你可以使用 `turnLeft()` 來左轉，但若是要右轉呢？

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
moveForward()
moveForward()
moveForward()
turnLeft()
turnLeft()
turnLeft()
moveForward()
moveForward()
moveForward()
collectGem()
```

## 後記

完成這關後，有沒有發現，如果我們要右轉，就會需要重複三次的 `turnLeft()`，在下一關中，我們將會學習如何使用函數來解決這個問題。

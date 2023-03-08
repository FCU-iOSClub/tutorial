# 切換開關

目標：收集寶石，然後切換開關狀態。

## 簡介

到目前為止，你已經學習了如何讓 Byte 四處移動和收集寶石。在這個關卡中，你將使用另一個新指令：`toggleSwitch()`。

<!-- prettier-ignore -->
!!! info "開關"
    開關可以切換為兩種狀態：**開啟**或**關閉**。

![toggling-a-switch](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/c835f4ec-a3b2-4002-a77a-5584670da600/public)

## 講解

在這一關，你需要學習如何使用新的指令 `toggleSwitch()`，這個指令可以讓 Byte 切換開關的狀態。你需要讓 Byte 收集到寶石之後，使用 `toggleSwitch()` 切換開關的狀態。

## 解答

<!-- prettier-ignore -->
--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
moveForward()
moveForward()
turnLeft()
moveForward()
collectGem()
moveForward()
turnLeft()
moveForward()
moveForward()
toggleSwitch()
```

## 後記

恭喜你完成了這一關的挑戰！通過不斷的學習和實踐，相信你已經對程式設計有了更深入的了解。現在，讓我們繼續挑戰下一關，挑戰更多的難題，並不斷提升自己的技能和能力。加油！

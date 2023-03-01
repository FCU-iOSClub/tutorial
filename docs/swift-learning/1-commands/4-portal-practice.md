# 傳送門練習

挑戰：通過傅送門來收集寶石。

## 簡介

在你的第一項挑戰中，新的元件出現在 Byte 的世界裡。傳送門可將 Byte 從某個地方傳送到另一個地方，Byte 進出傳送門時會面朝同一個方向。

你需要依照正確的順序運用目前學習的所有指令來打開開關、穿過傳送門以及收集寶石。

不要擔心第一次不成功。把這當成一次試驗的機會！

![portal-practice](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/1be61420-099a-4f9e-b89e-5060f3532f00/public)

## 講解

傳送門也會是將來單元中的重要元件，所以在這一關中，你需要學習如何使用傳送門來完成解題。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
moveForward()
moveForward()
moveForward()
turnLeft()
moveForward()
moveForward()
toggleSwitch()
moveForward()
moveForward()
turnLeft()
moveForward()
moveForward()
collectGem()
```

## 後記

對於初學者來說，可能需要透過多次嘗試來找到最佳的解答方式。這時候，可以思考一下程式碼是否可以簡化或者優化。可以嘗試修改原本的解答，看看是否能夠更簡潔、更有效率地完成任務。

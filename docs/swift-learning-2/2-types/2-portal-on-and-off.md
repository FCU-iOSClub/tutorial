# 開啓和關閉傳送門

打開和關閉傳送門來收集寶石與切換開關。

## 簡介

在這項挑戰中，你需要使用傳送門，走到關卡世界中的另一個位置，也要穿過傳送門來到達一些位置。
在適當的時機打開和關閉傳送門，藉此來練習設定屬性。在這個關卡中，有一種稱為 purplePortal 的實例，你可以使用點記法來修改它。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/cdc83a12-8594-4832-03a6-7573121fee00/public)

## 講解

在實例名稱 purplePortal 後方加上句點（.），以及想要存取的屬性名稱 (isActive)。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
purplePortal.isActive = false
func moveThree() {
    moveForward()
    moveForward()
    moveForward()
}
for i in 1...3 {
    moveThree()
    turnRight()
    moveThree()
    toggleSwitch()
    turnLeft()
    turnLeft()
}
```

## 後記

執行程式碼時，有時需要多次修改實例的屬性。做得很棒！

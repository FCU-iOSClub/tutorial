# 製作你自己的傳送門

目標：加入一個傳送門來跳到不同的區域。

## 簡介

你已經使用過傳送門在關卡世界各個區域之間傳送。在這個關卡中，你將在兩座漂浮的島嶼之間建立傳送門。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/ea6d4105-fbc5-4277-92c2-c9c5accb3700/public)

## 講解

首先，需要建立一個 Portal 類型的實例，並傳入顏色資訊。接著，指定傳送門起點側和終點側的座標來放置傳送門。範例如下:

放置傳送門
```swift linenums="1"

world.place(newPortal, atStartColumn: 1, startRow: 1, atEndColumn: 2, endRow: 2)
```
1. 呼叫 place 方法來放置傳送門，此方法包括參數 atstartcolumn 、 startRow 、 atEndColumn 和 endRow 。
2. 使用傳送門從一座島嶼跳到另一座島嶼，並收集所有寶石。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let greenPortal = Portal(color: .green)
world.place(greenPortal, atStartColumn: 1, startRow: 5, atEndColumn: 5, endRow: 1)
var gemCounter = 0
while gemCounter < 8 {
    moveForward()
    if gemCounter == 4 {
        turnLeft()
        turnLeft()
    } else {
        turnLeft()
    }
    moveForward()
    collectGem()
    gemCounter = gemCounter + 1
    turnLeft()
    turnLeft()
}
```

## 後記

你正在成為一位世界構建達人！

既然你知道如何放置傳送門，那麼離使用程式碼構建整個關卡世界又邁進了一步。接下來，你將放置一些階梯。 

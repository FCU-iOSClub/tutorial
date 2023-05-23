# 附加到陣列

目標：依據座標屬性來附加到空的陣列。

## 簡介

將項目個別加入陣列中，存粹是重複性的操作。要是能夠建立一套規則來將座標包含在陣列中呢？

首先，從`allCoordinates`開始，這是由關卡世界中所有座標組成的**陣列**

接著，你需要一個空的陣列，讓這些座標可以附加在其中。由於要**宣告**一個未儲存任何值的陣列，因此需要指定它應該容納的項目**類型**

>建立空的陣列
>
>在變數名稱後使用：來宣告其類型，然後將它**指定**為空的陣列。
>
>`var newLocations: [Coordinate] = []`

最後，**反覆運算**`allCoordinates`並檢查每個座標的`column`和`row`**屬性**。如果座標的`column`屬性大於5或`row`屬性小於4，則將它附加到空的陣列中。然後將六個磚塊放置在陣列中的每個座標上。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/35124c1a-b596-4982-fdc3-3724eaa6fd00/public)

## 講解

首先，要將範圍內的值（座標的`column`屬性大於5或`row`屬性小於4）加入｀append`到blockSet中。

接著，將陣列blockSet中的座標加上6磚塊（可用for-in迴圈重複執行6次）

最後，就能順利達成關卡目標了！

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let allCoordinates = world.allPossibleCoordinates
var blockSet: [Coordinate] = []
for coordinate in allCoordinates {
    if coordinate.column > 5 || coordinate.row < 4 {
        blockSet.append(coordinate)
    }
}
for coordinate in blockSet {
    for i in 1 … 6 {
        world.place(Block(), at: coordinate)
    }
}
```

## 後記

很好！
陣列會引領你走向建構世界的新世界！請記住，你可以建立完全空白的陣列，稍後再向其中加入值，辦事你必須指明該陣列包含的項目類型。當你**宣告**陣列時，請使用下列**語法**為它指定類型：

`var placementLocations: [Coordinate]`。

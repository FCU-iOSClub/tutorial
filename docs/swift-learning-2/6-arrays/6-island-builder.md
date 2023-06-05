# 島嶼建構者

挑戰：建構一座四面環海的島。

## 簡介

厭倦了內陸世界嗎？使用程式碼來創造你自己的島嶼！

首先，建立兩個用來儲存座標的空**陣列**。其中一個儲存島嶼的座標，另一個則儲存海洋的座標。

接著，在 **if 語句**中編寫一組條件，將座標附加到島嶼陣列中。這些座標應該位於地圖的中心，而且可能是3x3或4x4的磚塊。將不符合這些條件的所有座標附加到海洋的陣列中。

>加入水
>
>若要加入水，請先移除現有的磚塊。
>
>`world.removeAllBlocks(at: coordinate)`
>
>`world.place(Water(), at: coordinate)`

將座標附加到每個陣列後，在島嶼陣列的每個座標上放置磚塊，並在海洋陣列的每個座標上放置水。祝你好運！


![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/b1d5dc48-cc83-4128-00fc-de600dc24f00/public)

## 講解

1. 先建立兩個陣列來存放陸地和海洋的位置  

2. 使用 `if-else` 判斷，將陸地和海洋位置分別新增至兩個陣列

3. 在 `for` 迴圈中執行海洋陣列中有的座標位置，並將這些位置的陸地移除並加上水

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let allCoordinates = world.allPossibleCoordinates
// Create two empty arrays of type [Coordinate].
var island: [Coordinate] = []
var sea: [Coordinate] = []
for coordinate in allCoordinates {
    if coordinate.column >= 3 && coordinate.column < 7 && coordinate.row > 3 && coordinate.row < 7 {
        island.append(coordinate)
    } else {
        sea.append(coordinate)
    }
}
// For your island, array, place blocks.
for coordinate in island {
    for i in 1...4 {
        world.place(Block(), at: coordinate)
    }
}
// For your sea, array, place water.
for coordinate in sea {
    world.removeAllBlocks(at: coordinate)
    world.place(Water(), at: coordinate)
}
```

## 後記

你的能力不斷增強！

你可以使用陣列既快速又有效地管理大量資訊，進而建構精彩的世界。

你有沒有注意到陣列 `allCoordinates` 如何被初始化？你可以使用 world 實例的 `allPossibleCoordinates` **屬性**取得關卡世界中所有座標的陣列，藉此反覆運算每個座標。是不是很酷呢？


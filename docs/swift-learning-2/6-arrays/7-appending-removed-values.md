# 附加到移除的值

目標：將座標從一個障列中移除。並附加到另一個陣列中。

## 簡介

有時你可能會想要使用從陣列中移除的項目。還好，移除的項目會暫時儲存下來，因此你可以將它分配給一個變数或附加到另一個陣列中。

> 範例
>
> `var rightColumn = world.column (7)`
>
> `newArray.append(rightColumn.remove(at: 1))`

在上方的程式碼中，附加到 `newArray` 的座標就是從 `rightColumn`中移除的座標。

你可能已經注意到。`rightColumn` 是透過方法來進行初始化。`world` 實例中包含一組 `方法`，可讓你快速建立包含一個直欄或横列中所有座標的陣列。

> 呼叫方法來建立陣列
>
> `var row = world.row(1)`
>
> `var column5 = world.column(5)`
>
> `var topRows = world.coordinates(inRows: [5,6,7])`
>
> `var allCoords = wor1d.allPossibleCoordinates`


1. 建立一個空的座標陣列。並使用方法來建立另一個由横列 `2` 中所有座標構成的陣列。
2. 每次 `外迴國` 執行時，從陣列中移除一個項目並將其附加到空的陣列中。
3. 反覆運算空陣列，在每個座標處放置一個 `Character` 類型的實例。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/f1fbb924-a757-47a5-2c20-a8f06cc8d600/public)

## 講解

在簡介中可以很清楚知道程式撰寫的步驟，有時候也有需要撰寫與規格書相同的程式，試著依照指示來寫吧～

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
// Create an array of all coordinates in row 2
var row2 = world.coordinates(inRows: [2])
// Create an empty array of coordinates
var discardedCoordinates: [Coordinate] = []
for i in 1...12 {
    for coordinate in row2 {
        world.place(Block(), at: coordinate)
    }
    // Remove a coordinate and append it to your empty array
    discardedCoordinates.append(row2.remove(at: 0))
}
// Place a character for each coordinate added to your empty array.
for coordinate in discardedCoordinates {
    world.place(Character(), at: coordinate)
}
```

## 後記

愈來愈厲害了！

你知道嗎？初始化 `Character` 實例時，你可以透過 `name` 參數來選擇要使用的角色。初始化角色時，傳入以下三個列舉
選項中的其中一個：

> `character (name : .byte)`
>
> `Character (name: .blu)`
>
> `Character (name: .hopper)`

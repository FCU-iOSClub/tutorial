# 堆疊磚塊

目標：在每個角落放置五層磚塊。

## 簡介

查看下列程式碼。這是一個`Coordinate`類型的陣列，而不是**Int**值的陣列。
>`Coordinate類型`
>
>`Coordinate`實例使用`column`和`row`引數來參照一個位置。
>
>`let corner =  Coordinate(column: 3,row: 3)`

你可以使用`blockLocations`陣列反覆運算每個座標，並在每個位置上執行某項操作，例如：
>範例
>
>```
>for coordinate in blockLocations{
>   world.place(Gem(), at: coordinate)
>}
>```

1   加入了兩個座標到`blockLocations`中，每個座標參照世界中剩於的角落。

2   使用`for-in`迴圈**反覆運算**每個座標，在每個角落放置**五個磚塊**。（你可能需要**嵌套**其他**for迴圈**。)


![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/25f474c7-9bc0-4d77-d150-1d4f3faa0200/public)

## 講解
首先，將四個角落的位置加入`blockLocations`陣列中。

接著，試著在迴圈中再加入一個迴圈，並重複執行五次堆疊磚塊的動作，就能輕鬆完成目標！

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let blockLocations = [
    Coordinate(column: 0, row: 0),
    Coordinate(column: 3, row: 3),
    Coordinate(column: 0, row: 3),
    Coordinate(column: 3, row: 0),
]
for coordinate in blockLocations {
    for i in 1...5 {
        world.place(Block(), at: coordinate)
    }
}
```

## 後記

好極了！

你可能已經注意到，place(item: Item, at:Coordinate)**方法**採用了Coordinate類型的輸入，而place(item: Item, atColumn: Int, row: Int)則採用兩個**Int**值。這兩種方法都可以用來放置項目，但在本章節中，你將使用place(item: Item, at: Coordinate)，因為要配合Coordinate類型的陣列一起使用。

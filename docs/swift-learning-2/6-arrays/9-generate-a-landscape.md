# 產生地形

目標：使用整數陣列來產生地形

## 簡介

這頁下方的程式碼包含兩個陣列：`heights` 儲存 Int 值，`al1coordinates` 儲存關卡世界中的所有座標。

使用 `heights` 陣列來決定在 `a11Coordinates` 中的每個座標上放置多少磚塊。為此，你需要存取 `heights` 中每個索引的特定 `Int` 值。

> 存取索引的值
>
> `var heights = [7,3,2,4]`
>
> `for i in 1...heights[0]`

由於索引 `0` 的 `heights` 值為 `7`， 因此 for 迴圈將執行 `7` 次。現在，要是想在每個座標上存取不同的索引呢？你需要將索引值儲存為變數並進行遞增。

> 範例
> ```
> var index = 0
> for coordinate in allCoordinates {
>   for i in 1...heights[index]{
>       world.place (Block(), at: coordinate)
>   }
>   index += 1
> }
>```

要注意。如果 `index` 的值比 `heights` 陣列中的項目數還要大，則會嘗試存取一個不存在的值，因而導致 `索引越界錯誤` 。只要確保 `index` 值絕對不會大於陣列中的項目數 `heights.count` 即可避免這種錯誤。

> 範例
>```
> if index == heights.count {
>   index = 0
> }
>```

1. 填入下列程式碼中缺少的部分，將不同高度的磚垛放置在每個座標上
2. 注意使用 `count` 屬性以避免陣列越界錯誤的部分。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/dbd93ba8-6ff3-4f51-1e2d-99a97bf69500/public)

## 講解

透過 heights 的陣列與 for 迴圈的操作也是很重要的一環，同時也要注意索引越界錯誤喔

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
var heights: [Int] = [1, 0, 8, 9, 4, 3, 1, 6, 12, 5]
let allCoordinates = world.allPossibleCoordinates
var index = 0
for coordinate in allCoordinates {
    if index == heights.count {
        index = 0
    }
    for i in 0...heights[index] {
        world.place(Block(), at: coordinate)
    }
    index += 1
}
```

## 後記

哇！你太厲害了！

你注意到了要如何避免越界錯誤嗎？例如，若陣列中的值為 10，表示你可以存取的最大索引值為 9 (因為索引由 0 開始)。

如果 index 變數等於 height.count (值 10)，那麽你將嘗試存取索引 10，餓就將會導致陣列越界。相反的，你可以在 index 變數的值等於陣列的項目數時將它還原成 0。。

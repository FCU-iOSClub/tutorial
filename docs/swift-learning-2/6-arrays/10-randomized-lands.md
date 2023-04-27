# 隨機化的陸地

挑戰：使用隨機化來創造獨特的世界

## 簡介

若你要使用 `heights` 陣列中的隨機值，那麼每次執行程式碼時都會產生什麼樣的獨特地形？

`randomInt` 函數會使用你傳入的值產生一個隨機的 `整數` 。在下列程式碼中，`for 迴圈` 内部 `定義` 了 `1ocalNumber` 。 每次執行迴國時，都會產生一個新的數字並附加到 `heights` 中。
> 範例
>```
> for i in 1...20 {
>   let localNumber = randomInt (from: 0, to: 12)
>   heights.append (localNumber)
> }
>```

在函數數或迴圈等程式碼結構内部定義的變數稱為 `區域變數`。就像上方的 `1oca1Number` 一樣，區域變數只存在於它被定義的程式碼結構內部。不可以用於程式碼中的其他任何位置。

在這項挑戰中，請使用 `randomInt` 函數以及你的陣列和條件碼知識，在每次執行程式碼時產生獨特的地形。請發揮創意，並且玩得開心！

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/218b51c7-bdec-40db-4d5d-d169cb410800/public)

## 講解

可以透過自己想要的方式建構你的世界，你可以使用之前所用到的函式或是可以使用自己的規則，祝你玩的愉快～

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let allCoordinates = world.allPossibleCoordinates
var heights: [Int] = []
// Append random numbers to heights.
for i in 1...12 {
    heights.append(randomInt(from: 0, to: 8))
}
var index = 0
for coordinate in allCoordinates {
    if index == heights.count {
        index = 0
    }

    // currentHeight stores the height at the current index.
    var currentHeight = heights[index]

    if currentHeight == 0 {
        // Do something interesting if currentHeight is equal to 0.
        world.removeItems(at: coordinate)

    } else {
        for i in 1...currentHeight {
            world.place(Block(), at: coordinate)
        }
        if currentHeight > 5 {
            // Do something different, such as placing a character.
            world.place(Character(), at: coordinate)

        } else if coordinate.column >= 3 && coordinate.column < 6 {
            // Do something different, such as placing water.
            world.removeItems(at: coordinate)
            world.place(Water(), at: coordinate)

        }
        // Add more rules to customize your world.

    }
    index += 1

}
```

## 後記

多棒的傑作！

隨機化能讓你每一次執行程式碼時都產生稍微不同的結果。除了產生隨機整數，你還可以使用 `randomBool()` 函數建立隨機  `布林值` (true 或 false)。以下是你可能使用的方法：

> 使用隨機布林值
>```
> if randomBool() {
>   world.removeAllBlocks(at: coordinate)    
> }
>```

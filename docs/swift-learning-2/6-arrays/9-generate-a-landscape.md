# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/dbd93ba8-6ff3-4f51-1e2d-99a97bf69500/public)

## 講解

TODO

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

TODO

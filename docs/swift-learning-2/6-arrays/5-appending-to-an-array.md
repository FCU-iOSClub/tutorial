# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/35124c1a-b596-4982-fdc3-3724eaa6fd00/public)

## 講解

TODO

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

TODO

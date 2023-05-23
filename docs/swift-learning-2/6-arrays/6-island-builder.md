# 島嶼建構者

挑戰：建構一座四面環海的島。

## 簡介

厭倦了內陸世界嗎？

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/b1d5dc48-cc83-4128-00fc-de600dc24f00/public)

## 講解

TODO

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

TODO

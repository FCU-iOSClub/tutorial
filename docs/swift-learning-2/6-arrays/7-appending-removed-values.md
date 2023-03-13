# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/f1fbb924-a757-47a5-2c20-a8f06cc8d600/public)

## 講解

TODO

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

TODO

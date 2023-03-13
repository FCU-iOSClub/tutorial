# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/25f474c7-9bc0-4d77-d150-1d4f3faa0200/public)

## 講解

TODO

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

TODO

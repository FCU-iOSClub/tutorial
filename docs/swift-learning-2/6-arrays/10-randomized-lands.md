# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/218b51c7-bdec-40db-4d5d-d169cb410800/public)

## 講解

TODO

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

TODO

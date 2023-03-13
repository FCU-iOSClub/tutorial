# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/ea6d4105-fbc5-4277-92c2-c9c5accb3700/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let greenPortal = Portal(color: .green)
world.place(greenPortal, atStartColumn: 1, startRow: 5, atEndColumn: 5, endRow: 1)
var gemCounter = 0
while gemCounter < 8 {
    moveForward()
    if gemCounter == 4 {
        turnLeft()
        turnLeft()
    } else {
        turnLeft()
    }
    moveForward()
    collectGem()
    gemCounter = gemCounter + 1
    turnLeft()
    turnLeft()
}
```

## 後記

TODO

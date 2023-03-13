# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/6f94203e-eaab-44d8-3dc5-0fc2ff64e800/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let expert = Expert()
func solveSide() {
    expert.moveForward()
    expert.moveForward()
    expert.moveForward()
    if expert.isOnGem {
        expert.collectGem()
    } else {
        expert.turnLockUp()
    }
}
func returnToCenter() {
    expert.turnLeft()
    expert.turnLeft()
    expert.moveForward()
    expert.moveForward()
    expert.moveForward()
    expert.turnRight()
}
for i in 1...3 {
    solveSide()
    returnToCenter()
}
solveSide()
```

## 後記

TODO

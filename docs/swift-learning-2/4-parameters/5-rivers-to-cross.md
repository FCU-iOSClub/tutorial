# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/929a9dce-c05d-4026-15aa-b26a70d02900/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let expert = Expert()
world.place(
    expert, facing: .south,
    atColumn: 1, row: 8)
func collectGemsInLine() {
    while !expert.isBlocked {
        if expert.isOnGem {
            expert.collectGem()
        }
        expert.moveForward()
    }
}
collectGemsInLine()
expert.turnLockDown()
expert.turnLeft()
collectGemsInLine()
expert.turnLockUp()
expert.turnRight()
collectGemsInLine()
```

## 後記

TODO

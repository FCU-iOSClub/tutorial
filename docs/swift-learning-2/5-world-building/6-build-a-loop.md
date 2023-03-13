# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/ae7a952f-38a3-4d0e-9802-59846545b600/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let totalGems = randomNumberOfGems
var gemCounter = 0
world.place(Block(), atColumn: 0, row: 2)
world.place(Block(), atColumn: 3, row: 3)
let expert = Expert()
world.place(expert, facing: east, atColumn: 2, row: 3)
while gemCounter < totalGems {
    if expert.isOnGem {
        expert.collectGem()
        gemCounter = gemCounter + 1
    }
    if expert.isBlocked {
        expert.turnRight()
        if expert.isBlocked {
            expert.turnRight()
            if expert.isBlocked {
                expert.turnRight()
            }
        }
    }
    expert.moveForward()
}
```

## 後記

TODO

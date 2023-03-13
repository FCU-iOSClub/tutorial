# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/83af3e53-4ed4-4ed9-7359-3db7372b6700/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let topExpert = Expert()
let bottomExpert = Expert()
world.place(topExpert, facing: north, atColumn: 0, row: 4)
world.place(bottomExpert, facing: east, atColumn: 0, row: 0)
bottomExpert.collectGem()
bottomExpert.move(distance: 3)
bottomExpert.turnLeft()
bottomExpert.turnLock(up: true, numberOfTimes: 2)
bottomExpert.turnRight()
topExpert.turnLockDown()
bottomExpert.move(distance: 3)
bottomExpert.turnLock(up: false, numberOfTimes: 2)
topExpert.turnRight()
while !topExpert.isBlocked {
    if topExpert.isOnGem {
        topExpert.collectGem()
    }
    topExpert.moveForward()
}
```

## 後記

TODO

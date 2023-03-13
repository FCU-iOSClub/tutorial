# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/cd76dbd6-d0de-485a-7b20-923b9c9c3500/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let totalGems = randomNumberOfGems
var gemCounter = 0
while gemCounter < totalGems {
    if isOnGem {
        collectGem()
        gemCounter = gemCounter + 1
    }
    if isBlocked {
        turnRight()
        if isBlocked {
            turnLeft()
            turnLeft()
            if isBlocked {
                turnLeft()
            }
        }
    }
    moveForward()
}
```

## 後記

TODO

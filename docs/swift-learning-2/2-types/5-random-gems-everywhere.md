# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/e4a47d56-fe70-4326-d600-f21bb13af200/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let totalGems = randomNumberOfGems
var gemCounter = 0
bluePortal.isActive = false
pinkPortal.isActive = false
while gemCounter < totalGems {
    if isOnGem {
        collectGem()
        gemCounter = gemCounter + 1
    }
    moveForward()
    if isBlocked {
        turnLeft()
        turnLeft()
        if bluePortal.isActive == true {
            bluePortal.isActive = false
            pinkPortal.isActive = false
        } else if bluePortal.isActive == false {
            bluePortal.isActive = true
            pinkPortal.isActive = true
        }
    }
}

```

## 後記

TODO

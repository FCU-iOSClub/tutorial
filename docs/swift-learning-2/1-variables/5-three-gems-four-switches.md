# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/1b411196-e4da-4a39-aed1-6aa7d4130700/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
var gemCounter = 0
var switchCounter = 0
while gemCounter != 3 || switchCounter != 4 {
    if gemCounter != 3 && isOnGem {
        collectGem()
        gemCounter = gemCounter + 1
    } else if switchCounter != 4 && isOnClosedSwitch {
        toggleSwitch()
        switchCounter = switchCounter + 1
    }
    if isBlocked {
        turnRight()
        if isBlocked {
            turnLeft()
            turnLeft()
        }
    }
    moveForward()
} 
```

## 後記

TODO

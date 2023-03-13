# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/ce07548c-c477-46da-76ab-71abc6e6b100/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
var gemCounter = 0
var switchCounter = 0
while !isOnClosedSwitch {
    while !isBlocked {
        if isOnGem {
            collectGem()
            gemCounter = gemCounter + 1
        }
        moveForward()
    }
    turnRight()
}
while switchCounter < gemCounter {
    while !isBlocked {
        if isOnClosedSwitch && switchCounter < gemCounter {
            toggleSwitch()
            switchCounter = switchCounter + 1
        }
        moveForward()
    }
    turnRight()
}
```

## 後記

TODO

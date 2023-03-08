# TODO

TODO:TODO

## 簡介

TODO

![img](https://ppt.cc/fddEQx)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
while !isOnOpenSwitch {
    moveForward()
    if isOnGem {
        collectGem()
        turnRight()
        moveForward()
        collectGem()
    } else if isOnClosedSwitch {
        toggleSwitch()
        turnLeft()
        moveForward()
        toggleSwitch()
    }
    while !isBlocked {
        moveForward()
    }
    if !isBlockedRight {
        turnRight()
    } else {
        turnLeft()
    }
}
```

## 後記

TODO

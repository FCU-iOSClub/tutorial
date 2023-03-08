# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/e3acd94f-6c05-44df-7dd4-1d0d630ad200/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
while !isOnGem {
    while !isOnClosedSwitch && !isOnGem {
        moveForward()
    }
    if isOnClosedSwitch && isBlocked {
        toggleSwitch()
        turnLeft()
    } else if isOnClosedSwitch {
        toggleSwitch()
        turnRight()
    }
}
collectGem()
```

## 後記

TODO

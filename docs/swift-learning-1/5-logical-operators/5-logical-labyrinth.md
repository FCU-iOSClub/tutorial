# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/b4c26d63-4c83-49b2-2bfa-6237daba5f00/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
for i in 1 ... 8 {
    moveForward()
    if isOnGem && isOnClosedSwitch {
        turnRight()
        moveForward()
        moveForward()
        collectGem()
        turnLeft()
        turnLeft()
        moveForward()
        moveForward()
        turnRight()
        collectGem()
        toggleSwitch()
    } else if isOnClosedSwitch {
        turnLeft()
        toggleSwitch()
    }
    if isOnGem {
        collectGem()
    }
}
```

## 後記

TODO

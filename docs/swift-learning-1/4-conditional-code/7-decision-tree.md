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
func solveRightSide() {
    collectGem()
    turnRight()
    moveForward()
    moveForward()
    moveForward()
    turnLeft()
    moveForward()
    collectGem()
    turnLeft()
    turnLeft()
    moveForward()
    turnRight()
    moveForward()
    moveForward()
    moveForward()
    turnRight()
}
for i in 1...5 {
    moveForward()
    if isOnGem {
        solveRightSide()
    } else if isOnClosedSwitch {
        toggleSwitch()
        turnLeft()
        moveForward()
        collectGem()
        turnLeft()
        turnLeft()
        moveForward()
        turnLeft()
    }
}
```

## 後記

TODO

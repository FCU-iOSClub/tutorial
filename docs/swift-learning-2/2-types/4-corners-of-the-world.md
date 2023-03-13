# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/f310438a-4cc1-4092-27ad-2e52f5385700/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func turnAround() {
    turnLeft()
    turnLeft()
}
func checkSquare() {
    if isOnGem {
        collectGem()
    } else if isOnClosedSwitch {
        toggleSwitch()
    }
}
func collectOrToggle() {
    moveForward()
    checkSquare()
    turnAround()
}
func collectOrToggleThenTurnRight() {
    collectOrToggle()
    moveForward()
    turnRight()
}
func collectOrToggleThenTurnLeft() {
    collectOrToggle()
    moveForward()
    turnLeft()
}
turnLeft()
moveForward()
moveForward()
greenPortal.isActive = false
for i in 1...3 {
    collectOrToggleThenTurnRight()
}
collectOrToggle()
greenPortal.isActive = true
moveForward()
greenPortal.isActive = false
collectOrToggleThenTurnLeft()
collectOrToggleThenTurnLeft()
moveForward()
moveForward()
orangePortal.isActive = false
moveForward()
for i in 1...3 {
    collectOrToggleThenTurnRight()
}
collectOrToggle()
orangePortal.isActive = true
moveForward()
orangePortal.isActive = false
turnLeft()
collectOrToggleThenTurnRight()
collectOrToggle()
```

## 後記

TODO

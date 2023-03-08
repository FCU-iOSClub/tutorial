# 寶石農場

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/53fdd469-c3ce-48f9-de17-b38464d2cb00/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func turnAround() {
    turnLeft()
    turnLeft()
    moveForward()
    moveForward()
}
func solveRow() {
    turnRight()
    moveForward()
    collectGem()
    moveForward()
    collectGem()
    turnAround()
    moveForward()
    toggleSwitch()
    moveForward()
    toggleSwitch()
    turnAround()
    turnLeft()
    moveForward()
}
for i in 1...3 {
    solveRow()
}
```

## 後記

TODO

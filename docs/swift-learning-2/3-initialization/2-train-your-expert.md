# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/0a2006a7-2964-4b91-c5b1-e0595cebc900/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let expert = Expert()
func turnAround() {
    expert.turnLeft()
    expert.turnLeft()
    expert.moveForward()
    expert.moveForward()
}
func completeSide() {
    expert.moveForward()
    expert.moveForward()
    expert.collectGem()
}
for i in 1...2 {
    completeSide()
    turnAround()
    expert.turnRight()
}
completeSide()
expert.turnLockDown()
turnAround()
expert.turnRight()
for i in 1...3 {
    expert.moveForward()
}
expert.turnLeft()
for i in 1...3 {
    completeSide()
    turnAround()
    expert.turnLeft()
}
```

## 後記

TODO

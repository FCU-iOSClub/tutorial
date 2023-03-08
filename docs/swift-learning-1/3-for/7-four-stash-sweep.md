# 橫掃四方

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/f08228ec-aa90-475c-390a-f2e4bc374200/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func turnAround() {
    turnRight()
    turnRight()
}
func collectFour() {
    collectGem()
    moveForward()
    collectGem()
    turnAround()
    moveForward()
    turnRight()
    moveForward()
    collectGem()
    turnAround()
    moveForward()
    moveForward()
    collectGem()
}
moveForward()
for i in 1...3 {
    collectFour()
    moveForward()
    moveForward()
}
collectFour()
```

## 後記

TODO

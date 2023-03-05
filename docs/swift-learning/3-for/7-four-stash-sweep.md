# 橫掃四方

TODO:TODO

## 簡介

TODO

![img](https://unsplash.com/photos/NodtnCsLdTE/download?ixid=MnwxMjA3fDB8MXxzZWFyY2h8MTd8fGNhdHxlbnwwfHx8fDE2Nzc5OTU0MDg&force=true&w=1920)

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

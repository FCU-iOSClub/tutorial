# 拓展技能

TODO:TODO

## 簡介

TODO

![img](https://unsplash.com/photos/NodtnCsLdTE/download?ixid=MnwxMjA3fDB8MXxzZWFyY2h8MTd8fGNhdHxlbnwwfHx8fDE2Nzc5OTU0MDg&force=true&w=1920)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func traverseStairway() {
    for i in 1...7 {
        moveForward()
    }
}
func clearStairway() {
    traverseStairway()
    toggleSwitch()
    turnRight()
    turnRight()
    traverseStairway()
    turnRight()
}
for i in 1...3 {
    moveForward()
    moveForward()
    turnRight()
    clearStairway()
}
```

## 後記

TODO

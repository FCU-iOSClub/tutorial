# 拓展技能

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/7ece953d-11da-432e-e27a-c9b263ee5200/public)

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

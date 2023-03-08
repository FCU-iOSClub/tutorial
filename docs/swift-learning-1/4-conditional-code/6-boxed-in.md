# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/f07d6452-2d24-46eb-38e3-116b69995e00/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func checkSquare() {
    if isOnGem {
        collectGem()
    } else if isOnClosedSwitch {
        toggleSwitch()
    }
}
func completeCorner() {
     checkSquare()
     moveForward()
     checkSquare()
     turnRight()
     moveForward()
}
moveForward()
turnRight()
for i in 1...4 {
     completeCorner()
}
```

## 後記

TODO

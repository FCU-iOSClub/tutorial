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
func navigateAroundWall() {
    if isBlockedRight {
        moveForward()
    } else {
        turnRight()
        moveForward()
    }
}
while !isOnClosedSwitch {
    navigateAroundWall()
    if isOnGem {
        collectGem()
        turnLeft()
        turnLeft()
    }
}
toggleSwitch() 
```

## 後記

TODO

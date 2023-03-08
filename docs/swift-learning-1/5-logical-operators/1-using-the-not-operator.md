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
for i in 1...4 {
    moveForward()
    if !isOnGem {
        turnLeft()
        moveForward()
        moveForward()
        collectGem()
        turnLeft()
        turnLeft()
        moveForward()
        moveForward()
        turnLeft()
    } else {
        collectGem()
    }
}
```

## 後記

TODO

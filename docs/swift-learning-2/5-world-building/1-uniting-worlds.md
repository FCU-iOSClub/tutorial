# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/c8cbcf50-1823-49e4-cb43-8b6a3ba32200/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let block1 = Block()
world.place(block1, atColumn: 3, row: 3)
while !isOnClosedSwitch {
    moveForward()
    if isBlocked {
        turnLeft()
        if isBlocked {
            turnRight()
            turnRight()
        }
    }
}
toggleSwitch()
```

## 後記

TODO

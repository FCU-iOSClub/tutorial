# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/032018b0-2e37-4843-81a5-24074ef2ad00/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let block1 = Block()
let block2 = Block()
let block3 = Block()
let block4 = Block()
let block5 = Block()
world.place(block1, atColumn: 2, row: 2)
world.place(block2, atColumn: 2, row: 2)
world.place(block3, atColumn: 4, row: 2)
world.place(block4, atColumn: 6, row: 2)
world.place(block5, atColumn: 6, row: 2)
func crossBridge() {
    turnRight()
    move(distance: 4)
    collectGem()
    turnLeft()
    turnLeft()
    move(distance: 4)
    turnRight()
}
for i in 1...3 {
    move(distance: 2)
    toggleSwitch()
    crossBridge()
}
```

## 後記

TODO

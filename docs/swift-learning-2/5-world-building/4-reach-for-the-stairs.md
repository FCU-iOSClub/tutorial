# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/2b1f2ed1-6400-4bbe-fe7c-07b59c1bca00/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
world.place(Stair(), facing: south, atColumn: 3, row: 1)
world.place(Stair(), facing: south, atColumn: 3, row: 3)
world.place(Stair(), facing: west, atColumn: 1, row: 4)
world.place(Stair(), facing: west, atColumn: 1, row: 6)
world.place(Stair(), facing: east, atColumn: 5, row: 6)
world.place(Stair(), facing: north, atColumn: 2, row: 7)
world.place(Stair(), facing: north, atColumn: 4, row: 7)
func toggleSide() {
    toggleSwitch()
    while !isBlocked {
        moveForward()
        toggleSwitch()
    }
}
func turnCorner() {
    turnRight()
    move(distance: 2)
    turnLeft()
    move(distance: 2)
    turnRight()
}
move(distance: 4)
turnLeft()
move(distance: 3)
turnRight()
for i in 1...2 {
    toggleSide()
    turnCorner()
}
toggleSide()
```

## 後記

TODO

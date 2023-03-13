# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/4e01edf9-5ef4-45c6-a002-a172e274ac00/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let character = Character()
let expert = Expert()
world.place(character, facing: north, atColumn: 0, row: 0)
world.place(expert, facing: north, atColumn: 3, row: 0)
func collectAndJump() {
    for i in 1...2 {
        character.collectGem()
        character.jump()
        character.jump()
    }
}
expert.toggleSwitch()
expert.turnLockUp()
collectAndJump()
character.turnRight()
collectAndJump()
character.turnLeft()
character.collectGem()
character.move(distance: 2)
character.collectGem()
```

## 後記

TODO

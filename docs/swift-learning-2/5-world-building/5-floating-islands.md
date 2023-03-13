# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/09a77d97-9020-4208-9dcc-0024d0d1f300/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let character = Character()
world.place(character, facing: south, atColumn: 1, row: 7)
func completeIsland() {
    character.toggleSwitch()
    character.jump()
    character.collectGem()
    character.turnLeft()
    character.jump()
    character.toggleSwitch()
}
completeIsland()
world.place(character, facing: north, atColumn: 6, row: 3)
completeIsland()
world.place(character, facing: east, atColumn: 1, row: 1)
completeIsland()
```

## 後記

TODO

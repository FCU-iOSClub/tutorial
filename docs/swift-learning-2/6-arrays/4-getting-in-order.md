# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/e12033ea-49b9-42ba-58aa-b8b0385a2c00/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
var characters: [Item] = [
    Character(name: .blu),
    Portal(color: .pink),
    Character(name: .byte),
    Gem(),
    Character(name: .hopper),
]
// Remove the portal
characters.remove(at: 1)
// Remove the gem
characters.remove(at: 2)
// Insert the Expert behind Byte
characters.insert(Expert(), at: 1)
var rowPlacement = 0
for character in characters {
    world.place(character, at: Coordinate(column: 1, row: rowPlacement))
    rowPlacement += 1
}
```

## 後記

TODO

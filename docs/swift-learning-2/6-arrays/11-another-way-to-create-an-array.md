# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/6535d722-ca60-4b7d-96e1-4728f1803400/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let allCoordinates = world.allPossibleCoordinates
for coordinate in allCoordinates {
    let height = coordinate.column + coordinate.row

    for i in 0...height {
        world.place(Block(), at: coordinate)
    }

    if height >= 8 && height < 10 {
        world.place(Character(name: .blu), at: coordinate)
    } else if height > 9 {
        world.place(Character(name: .byte), at: coordinate)
    }
}
let characters = world.existingCharacters(at: allCoordinates)
for character in characters {
    character.jump()
}
```

## 後記

TODO

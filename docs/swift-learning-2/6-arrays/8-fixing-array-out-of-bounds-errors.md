# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/7bbbf70f-6746-4ab0-8103-321f5f862e00/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
var teamBlu: [Character] = []
// note how many characters are in your array
for i in 1...9 {
    teamBlu.append(Character(name: .blu))
}
var columnPlacement = 0
for blu in teamBlu {
    world.place(blu, at: Coordinate(column: columnPlacement, row: 4))
    columnPlacement += 1
}
// find the array out of bounds error
teamBlu[0].jump()
teamBlu[2].collectGem()
teamBlu[4].jump()
teamBlu[6].collectGem()
teamBlu[8].jump()
```

## 後記

TODO

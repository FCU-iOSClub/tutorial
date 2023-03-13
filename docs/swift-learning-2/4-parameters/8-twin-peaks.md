# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/4ca332bf-084e-4f68-8abb-57c5c0889a00/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let totalGems = randomNumberOfGems
let expert = Expert()
let character = Character()
world.place(expert, facing: north, atColumn: 0, row: 4)
world.place(character, facing: north, atColumn: 2, row: 0)
var gemCounter = 0
var platformPosition = 0
func jumpAcrossSide() {
    for i in 1...6 {
        if character.isOnGem && gemCounter < totalGems {
            character.collectGem()
            gemCounter = gemCounter + 1
        }
        character.jump()
    }
}
while gemCounter < totalGems {
    jumpAcrossSide()
    character.turnRight()
    if platformPosition == 0 {
        expert.turnLockUp()
        platformPosition = 1
    } else if platformPosition == 3 {
        expert.turnLock(up: false, numberOfTimes: 2)
        platformPosition = 1
    }
    character.moveForward()
    if character.isOnGem && gemCounter < totalGems {
        character.collectGem()
        gemCounter = gemCounter + 1
    }
    if platformPosition == 1 {
        expert.turnLock(up: true, numberOfTimes: 2)
        platformPosition = 3
    }
    character.moveForward()
    character.turnRight()
}
```

## 後記

TODO

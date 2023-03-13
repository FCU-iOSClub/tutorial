# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/cc3c5a60-3924-4b98-4005-1e76e47c7000/public)
 
## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let expert = Expert()
let character = Character()
func turnAround() {
    character.turnLeft()
    character.turnLeft()
}
func collectGemTurnAround() {
    character.moveForward()
    character.moveForward()
    character.collectGem()
    turnAround()
    character.moveForward()
    character.moveForward()
    character.turnRight()
}
for i in 1...4 {
    expert.turnLock(
        up: true,
        numberOfTimes: 4)
    expert.turnRight()
}
for i in 1...3 {
    while !character.isOnGem {
        character.moveForward()
    }
    character.collectGem()
    character.turnRight()
}
character.moveForward()
for i in 1...4 {
    expert.turnLock(
        up: false,
        numberOfTimes: 3)
    expert.turnRight()
}
character.turnLeft()
character.moveForward()
character.collectGem()
turnAround()
for i in 1...3 {
    character.moveForward()
    character.moveForward()
    if !character.isOnGem {
        character.turnRight()
        collectGemTurnAround()
    } else {
        character.collectGem()
    }
}
```

## 後記

TODO

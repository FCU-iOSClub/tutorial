# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/a02eba78-a22e-4c6f-45ce-e761e64b6f00/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let expert = Expert()
let character = Character()

func turnLock(up: Bool, numberOfTimes: Int) {
    for _ in 1...numberOfTimes {
        if up == true {
            expert.turnLockUp()
        } else {
            expert.turnLockDown()
        }
    }
}

func expertTurnAround() {
    expert.turnLeft()
    expert.turnLeft()
}

func characterTurnAround() {
    character.turnLeft()
    character.turnLeft()
}

turnLock(up: true, numberOfTimes: 3)
expertTurnAround()
turnLock(up: true, numberOfTimes: 3)
character.move(distance: 3)
character.collectGem()
characterTurnAround()
for i in 1...2 {
    character.moveForward()
    character.turnLeft()
}
turnLock(up: false, numberOfTimes: 3)
expertTurnAround()
turnLock(up: false, numberOfTimes: 2)
character.moveForward()
characterTurnAround()
character.collectGem()
character.moveForward()
expert.turnLockDown()
character.move(distance: 2)
character.collectGem()
```

## 後記

TODO

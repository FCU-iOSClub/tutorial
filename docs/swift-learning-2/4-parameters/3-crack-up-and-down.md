# 上下轉動

挑戰：使用專家和 `turnLock` **方法**來收集所有寶石。

## 簡介

在此關卡中，你可以使用 `turnLock` 和 `move` 來幫助角色收集所有寶石。通關的方式有很多種，因此，在開始前請花一些時間來思考幾種不同的方式。祝你好運！

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/cc3c5a60-3924-4b98-4005-1e76e47c7000/public)
 
## 講解

顯然這又是場硬仗，看見所有寶石了嗎？在上下層都有寶石需要搜集，不過不用擔心，現在開始可以直接使用 `move` 和 `turnLock` 函數了，可以試著將重複的動作做成函數，

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

太棒了，你現在已經學習了如何使用參數來建立函數，想想看如何使用參數將角色放置在關卡世界的特定位置。

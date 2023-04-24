# 雙峰

挑戰：運用你全部的程式設計技巧來收集數量隨機決定的寶石，以 `totalGems` 表示。

## 簡介

運用這項挑戰來測試你所掌握的參數、初始化、方法、變數和其他知識！在穿梭關卡世界收集寶石時，更多的寶石會隨機出現。你的目標是在收集完 `totalGems` 中指定的數量後便停止收集寶石。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/4ca332bf-084e-4f68-8abb-57c5c0889a00/public)

## 講解

總算來到這個章節的最後一個關卡了，這裡有個好消息與壞消息，好消息是沒有新的要學習的指令了，但壞消息是你必須用到先前所學的參數、初始化、方法、變數和其他知識才能夠順利過關，這是個嚴苛的考驗，不過也不需要緊張，你隨時能夠透過選單複習先前學習的內容，加油！這是本章節的最後關卡了！

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

太神啦，跳起來歡呼一下吧，你剛剛完成了參數！現在你掌握的程式設計知識足以改變整個關卡世界。感覺是不是很棒？現在是時候開始建構世界了。

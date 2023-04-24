# TODO

目標：編寫一個函數，以指定的次數向上或向下轉動鎖頭。

## 簡介

先前你曾使用**參數**來定義 `move` 函數，其中包含 `distance` 輸入。在這個關卡中，你將定義一個 `turnLock` 函數，使用參數 `up` 和 `numberOfTimes` 來決定專家應該轉動鎖頭的方向和次數。

> `解釋 turnLock 參數`
>
> `up` 使用 Bool (**布林值**) 類型的輸入，指示向上 (`true`) 或向下 (`false`) 轉動鎖頭。
>
> `numberofTimes` 使用 **Int** 類型的輸入，指示轉動鎖頭的次數。

1. 使用兩個參數 `up` `和numberofTimes` 來定義函數。
2. 檢查 up 的值來決定應該呼叫 `turnLockUp()` 還是 `turnLockDown()`。
3. 使用numberOfTimes 值來決定執行 `turnLockUp()` 或 `turnLockDown()` 的次數。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/a02eba78-a22e-4c6f-45ce-e761e64b6f00/public)

## 講解

在剛才你學會了參數的使用，但這個關卡中我們遇到了更加艱辛的問題，首先我們需要判斷鎖頭該如何解開，在此我們需要用到多個參數，`up` 以及 `numberOfTimes` ，在將參數傳入函數時別搞錯了他們對應的位置與型別。同時在該函數中用到了 `if else` 條件碼，若是忘記的同學不妨回到第一章複習一下喔！

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

在這次的挑戰中顯然遇到了更加困難的任務，因此也讓程式碼的行數增加許多，是不是發現到參數的重要性了呢，倘若沒辦法透過傳入參數化簡程式碼，那我想這會是場災難。現在你可以使用 `move` 和 `turnLock` `函數來通過之後的關卡了。可以使用點記法搭配Character` 和 `Expert` 類型來使用這些函數。範例：`expert.move(distance：4)` 和 `expert.turnLock(up: true, numberOfTimes: 2)`，每個函數都使用了這些新方法。
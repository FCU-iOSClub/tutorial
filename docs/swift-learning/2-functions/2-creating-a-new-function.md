# 產生新函數

目標：定義並使用你自己的函數來右轉。

## 簡介

在上一關中，你只右轉了一次，所以使用三次左轉不是問題。但如果你要右轉不止一次呢？更有效的方法是，將那些左轉動作納入一個 `turnRight()` 指令中，便於多次執行。

像 `turnRight()` 這樣的指令實際上是執行任務主體的函數。你一直都在使用函數。到目前為止，你使用過的每個指令實際上都是我們提供給你的函數，

若要定義一個函數，請在大括號 `{` 和 `}`之間輸入一組指令來指定它對應的動作。

1. 選取函數主體的內部（大括弧 `{` 和 `}` 之間）。
2. 輸入三個 `turnleft()` 指令，
3. 在函數下方，使用現有的指令以及 turnRight（）來打開關閉的開關

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/0959f3d1-b938-4bb6-7470-65b60acce300/public)

## 講解

終於要來創建我們的第一個函數了！在 `turnRight()` 中，填上適當的指令，讓角色右轉。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

<!-- prettier-ignore-start -->
=== "基礎解答"
    ```swift linenums="1"
    func turnRight() {
        turnLeft()
        turnLeft()
        turnLeft()
    }

    moveForward()
    turnLeft()
    moveForward()
    turnRight()
    moveForward()
    turnRight()
    moveForward()
    turnRight()
    moveForward()
    turnLeft()
    moveForward()
    toggleSwitch()
    ```
=== "進階解答"
    ```swift linenums="1"
    func turnRight() {
        turnLeft()
        turnLeft()
        turnLeft()
    }
    func goRight() {
        moveForward()
        turnRight()
    }
    func goLeft() {
        moveForward()
        turnLeft()
    }
    goLeft()
    goRight()
    goRight()
    goRight()
    goLeft()
    moveForward()
    toggleSwitch()
    ```
<!-- prettier-ignore-end -->

## 後記

上面的解答中，提供了多一種的進階解答，組合更多的指令，來讓程式碼更容易閱讀。同學以後也可以盡量嘗試使用這種方式來組合指令。

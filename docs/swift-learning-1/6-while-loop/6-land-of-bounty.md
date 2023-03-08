# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/6e53c455-cd79-432c-385a-541e9d41e800/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

<!-- prettier-ignore-start -->
=== "基礎解答"
    ```swift linenums="1"
    func solveColumn() {
        while !isBlocked {
            if isOnClosedSwitch {
                toggleSwitch()
            } else if isOnGem {
                collectGem()
            }
            moveForward()
        }
    }
    solveColumn()
    turnRight()
    moveForward()
    turnRight()
    solveColumn()
    turnLeft()
    moveForward()
    turnLeft()
    solveColumn()
    ```
=== "進階解答"
    ```swift linenums="1"
    func solveColumn() {
        while !isBlocked {
            if isOnClosedSwitch {
                toggleSwitch()
            } else if isOnGem {
                collectGem()
            }
            moveForward()
        }
    }
    func solveAndRightTurn() {
        solveColumn()
        turnRight()
    }
    solveAndRightTurn()
    moveForward()
    solveAndRightTurn()
    turnLeft()
    moveForward()
    turnLeft()
    solveColumn()
    ```
<!-- prettier-ignore-end -->

## 後記

TODO

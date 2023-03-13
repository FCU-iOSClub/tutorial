# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/a8f8f51f-2424-4eab-2ddb-728f4b0e1800/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

<!-- prettier-ignore-start -->
=== "基礎解答"
    ```swift linenums="1"
    let expert = Expert()
    func move(distance: Int) {
        for i in 1...distance {
            expert.moveForward()
        }
    }
    move(distance: 6)
    expert.turnRight()
    expert.move(distance: 2)
    expert.turnRight()
    move(distance: 5)
    expert.turnLeft()
    move(distance: 5)
    expert.turnLeft()
    expert.turnLockUp()
    expert.turnLeft()
    move(distance: 3)
    expert.turnRight()
    move(distance: 3)
    expert.turnRight()
    move(distance: 4)
    expert.collectGem()
    ```
=== "進階解答"
    ```swift linenums="1"
    let expert = Expert()
    func move(distance: Int) {
        for i in 1 … distance {
            expert.moveForward()
        }
    }
    func solvePuzzle(factorOrAddened: Int) {
        expert.move(distance: factorOrAddend * 3)
        expert.turnRight()
        expert.move(distance: factorOrAddend)
        expert.turnRight()
        for i in 1 … 2 {
            expert.move(
                distance:
                    factorOrAddend + 3)
            expert.turnLeft()
        }
        expert.turnLockUp()
        expert.turnLeft()
        for i in 1 … 2 {
            expert.move(
                distance:
                    factorOrAddend + 1)
            expert.turnRight()
        }
        expert.move(
            distance: factorOrAddend
                * 2)
        expert.collectGem()
    }
    solvePuzzle(factorOrAddend: 2)
    ```
<!-- prettier-ignore-end -->

## 後記

TODO

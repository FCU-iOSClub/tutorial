# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/a1cbf380-161b-4c40-e4c8-6d02cafa3b00/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

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
    world.place(expert, atColumn: 1, row: 1)
    expert.collectGem()
    world.place(expert, atColumn: 1, row: 6)
    expert.collectGem()
    world.place(expert, atColumn: 6, row: 1)
    expert.collectGem()
    ```
=== "進階解答"
    ```swift linenums="1"
    let expert = Expert()
    world.place(expert, atColumn: 2, row: 6)
    func turnAround() {
        expert.turnLeft()
        expert.turnLeft()
    }
    func turnLockCollectGem() {
        expert.turnLeft()
        expert.turnLockUp()
        turnAround()
        expert.moveForward()
        expert.collectGem()
        turnAround()
        expert.moveForward()
        expert.turnRight()
    }
    turnLockCollectGem()
    expert.move(distance: 5)
    turnLockCollectGem()
    expert.move(distance: 6)
    expert.collectGem()
    ```
<!-- prettier-ignore-end -->

## 後記

TODO


## 後記

TODO

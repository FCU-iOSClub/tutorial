# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/29aa68f4-1885-47ff-953f-1e11288e1700/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

<!-- prettier-ignore-start -->
=== "基礎解答"
    ```swift linenums="1"
    for i in 1...4 {
        moveForward()
        moveForward()
        moveForward()
        if isOnClosedSwitch {
            toggleSwitch()
        }
        turnRight()
    }
    ```
=== "進階解答"
    ```swift linenums="1"
    for i in 1...4 {
        for i in 1…3 {
            moveForward()
        }
        if isOnClosedSwitch {
            toggleSwitch()
        }
        turnRight()
    }
    ```
<!-- prettier-ignore-end -->

## 後記

TODO

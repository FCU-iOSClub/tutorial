# TODO

TODO:TODO

## 簡介

TODO

![img](https://ppt.cc/fddEQx)

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

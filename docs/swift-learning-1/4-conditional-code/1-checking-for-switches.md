# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/cbac3d0f-e3db-4be2-b42a-e24c89498700/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

<!-- prettier-ignore-start -->
=== "基礎解答"
    ```swift linenums="1"
    moveForward()
    moveForward()
    if isOnClosedSwitch {
        toggleSwitch()
    }
    moveForward()
    if isOnClosedSwitch {
        toggleSwitch()
    }
    moveForward()
    if isOnClosedSwitch {
        toggleSwitch()
    }
    ```
=== "進階解答"
    ```swift linenums="1"
    for i in 1…2 {
        moveForward()
    }
    for i in 1…2 {
        if isOnClosedSwitch {
            toggleSwitch()
        }
        moveForward()
    }
    if isOnClosedSwitch {
        toggleSwitch()
    }
    ```
<!-- prettier-ignore-end -->

## 後記

TODO

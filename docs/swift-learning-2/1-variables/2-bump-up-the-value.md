# TODO

TODO:TODO

## 簡介

TODO

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/e0d3d237-e3b9-4caa-4e75-dbd86d644100/public)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

<!-- prettier-ignore-start -->
=== "基礎解答"
    ```swift linenums="1"
    var gemCounter = 0
    moveForward()
    collectGem()
    gemCounter = 1
    moveForward()
    collectGem()
    gemCounter = 2
    moveForward()
    collectGem()
    gemCounter = 3
    moveForward()
    collectGem()
    gemCounter = 4
    moveForward()
    collectGem()
    gemCounter = 5
    ```
=== "進階解答"
    ```swift linenums="1"
    var gemCounter = 0
    while gemCounter <5 {
        moveForward()
        collectGem()
        gemCounter += 1
    }
    ```
<!-- prettier-ignore-end -->

## 後記

TODO

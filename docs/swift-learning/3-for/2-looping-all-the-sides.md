# 迴圈每一側

TODO:TODO

## 簡介

TODO

![img](https://unsplash.com/photos/NodtnCsLdTE/download?ixid=MnwxMjA3fDB8MXxzZWFyY2h8MTd8fGNhdHxlbnwwfHx8fDE2Nzc5OTU0MDg&force=true&w=1920)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

<!-- prettier-ignore-start -->
=== "基礎解答"
    ```swift linenums="1"
    for i in 1...4 {
        moveForward()
        collectGem()
        moveForward()
        moveForward()
        moveForward()
        turnRight()
    }
    ```
=== "進階解答"
    ```swift linenums="1"
    for i in 1...4 {
        moveForward()
        collectGem()
        for i in 1…3() {
            moveForward()
        }
        turnRight()
    }
    ```
<!-- prettier-ignore-end -->

## 後記

TODO

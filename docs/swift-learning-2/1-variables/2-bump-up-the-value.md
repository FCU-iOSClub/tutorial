# 當變數遇上收集寶石

目標:每多收集一個寶石就為 `gemCounter` 指定一個新的值。

## 簡介

你已經建立了一個變數定且更改它的值。在這項挑戰中，你將練習該技巧:
在收集更多寶石時正確地設定變數的值

指定 `gemCounter` 初始值為0。讓你的角色走到每顆寶石處並收集寶石。然後針對新收集的每顆寶石為 `gemCounter`指定正確的值

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/e0d3d237-e3b9-4caa-4e75-dbd86d644100/public)

## 講解

在這次挑戰中你需要建立一個變數名稱為`gemCounter` ，你需要讓Byte執行完`collectGem`後就重新更改一次`gemCounter`的值

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

恭喜完成這次挑戰!如果完成這次挑戰想必你對變數有一定的了解，往下一關繼續加把勁吧!

# 檢查開關

目標:使用if語句只切換關閉的開關。

## 簡介

在你編寫程式碼之前，你會注意到在走到上有三個開關，每一個都是隨機切換為開啟或關閉的。

1. 走到第一個開關。
2. 在快捷鍵中選取`if`來加入if語句。
3. 加入條件`isOnClosedSwitch`，並且在條件為真時切換開關。
4. 在剩下的兩個開關上重複相同的動作。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/cbac3d0f-e3db-4be2-b42a-e24c89498700/public)

## 講解

這題的目標是切換關閉的開關，在切換之前利用`if 語句`來檢查每個開關的狀態。在`if`語句中使用`isOnClosedSwitch`作為條件，來告訴Byte：「如果位於關閉的開關上，就切換開關。」

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

了不起！你剛剛編寫的程式碼即使不知道每個開關的狀態時也能正確執行。繼續探索更多使用`if語句`的方法吧！

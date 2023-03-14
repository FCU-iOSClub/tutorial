# 當...時執行程式碼

目標：使用迴圈，以在位於開關為打開的位置時繼續走動。

## 簡介

這一關有一排開關，關卡每次執行時開關的數量都不相同。與其讓你的角色走完全程並在每一步檢查是否需要打開開關，你不妨使用一種稱為 while 迴圈的條件碼。

就像 if 語句一樣，while 迴圈允許你決定何時執行你的程式碼。while 迴圈在布林值條件為真的情況下持續執行程式碼區塊。當條件為偽時， while 迴圈停止執行。

1. 為你的 while 迴圈選取一個布林條件，來確定其何時執行。
2. 在 while 區塊中加入指令來打開所有開關。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/bb6ae73b-582e-4f57-92c5-022885014f00/public)

## 講解

這題的目標為切換未打開的開關並往前走動，你需要學會如何決定 while 語句的條件才能打開所有開關。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

<!-- prettier-ignore-start -->
=== "解答 1"
    ```swift linenums="1"
    while isOnClosedSwitch {
        toggleSwitch()
        moveForward()
    }
    ```
=== "解答 2"
    ```swift linenums="1"
    while !isOnOpenSwitch {
        toggleSwitch()
        moveForward()
    }
    ```
<!-- prettier-ignore-end -->

## 後記

恭喜您完成了這一關的挑戰！這一關結合了條件和迴圈的概念，是一個非常重要的觀念。接下來會有許多變化的題目來加深您對這個概念的印象，相信您一定能夠應對自如。
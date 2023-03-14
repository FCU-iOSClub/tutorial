# 4 乘 4

挑戰：選擇最佳迴圈並切換開關。

## 簡介

在這項挑戰中，有數種方法可以通關，你可使用 while 迴圈、for 迴圈或者兩種類型的組合。
想出一個模式來打開每個開關，並且看看你使否能夠使用兩個迴圈的組合。你可以自己決定要使用的迴圈！

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/29aa68f4-1885-47ff-953f-1e11288e1700/public)

## 講解

在這題，可以停下來思考一下，哪一個步驟是重複的，可以再透過迴圈來精簡程式碼。

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

在這個挑戰中，我們學會了使用不同種類的迴圈來解決問題，而不只是依賴單一的解決方案。透過使用 while 迴圈和 for 迴圈，我們可以更加了解迴圈的特性和彈性，並且學會了如何結合兩種不同的迴圈來創造更多解決問題的可能性。

# 迴圈每一側

目標：使用一個 for 迴圈來重複指令序列。

## 簡介

在這個關卡中，你必須收集正方形周圍同樣相對位置上的四顆寶石。你要建立一個迴圈在每一個邊上重複下面的程式碼，以通過整個關卡

1. 在快捷鍵列中選取 for 來在程式碼中加入一個 for 迴圈。
2. 按下底部的大括號來選取迴圈
3. 按住大括號，然後將它往下拖來將現有的程式碼放入迴圈內。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/d4ddcad3-97b3-4ee7-03c9-76f003e05500/public)

## 講解

在解決這個挑戰時，同學們可以通過回顧已學過的相關知識去思考出最佳解決方案，繼而通過練習進一步鞏固技能。透過這樣的學習方式，同學們能夠加深對於 for 迴圈的理解和應用。

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

上方還提供了進階解答，展示了用嵌套迴圈的方式解決問題。同學們可以參考這個解答，並思考嵌套迴圈在開發中的應用。

回顧自己的寫法同樣很重要，這樣可以幫助同學們從中學習到自己的不足之處，也能夠對自己的程式碼進行改進和優化。另外，與其他人學習和分享代碼也是不錯的學習方式，因為可以從別人的方法中學到更多新的思路和技巧。

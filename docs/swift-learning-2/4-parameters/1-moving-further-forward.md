# 繼續前進

目標：編寫一個往前走特定步數的函數。

## 簡介

在這個關卡中使用一個新的函數，你可以用單一指令來走過多個磚塊，進而減少重複的程式碼。你將使用**參數**為函數指定一個輸入 `(distance)`。你呼叫函數時將為 `distance` 傳入一個值，或**引數**。例如，在 `move(distance: 6)` 中，`6` 為引數。

下方提供了 `move` 的函式宣告，其中包含參數 `distance` 。使用函數中的 `distance` 值來指定執行 `moveForward()` 的次數。當你呼叫 `move` 時，就會傳入 `distance` 的引數來執行`moveForward()` 的相應次數。

1. 填入函式定義，即在呼叫 `moveForward()` 指定次數的迴圈中使用 `distance` 參數。
2. 如果使用 **for迴圈** ，則將 `distance` 設為迴圈執行的次數。範例：`for i in 1. .. distance {`
3. 使用 `move` 函數來通關。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/a8f8f51f-2424-4eab-2ddb-728f4b0e1800/public)

## 講解

在這個章節，我們要學習透過傳入參數來更快的完成目標，首先你需要定義一個能夠傳入參數的函數，並且將原先使用的 `moveForward()` 取代為新定義的 `move()`。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

<!-- prettier-ignore-start -->
=== "基礎解答"
    ```swift linenums="1"
    let expert = Expert()
    func move(distance: Int) {
        for i in 1...distance {
            expert.moveForward()
        }
    }
    move(distance: 6)
    expert.turnRight()
    expert.move(distance: 2)
    expert.turnRight()
    move(distance: 5)
    expert.turnLeft()
    move(distance: 5)
    expert.turnLeft()
    expert.turnLockUp()
    expert.turnLeft()
    move(distance: 3)
    expert.turnRight()
    move(distance: 3)
    expert.turnRight()
    move(distance: 4)
    expert.collectGem()
    ```
=== "進階解答"
    ```swift linenums="1"
    let expert = Expert()
    func move(distance: Int) {
        for i in 1 … distance {
            expert.moveForward()
        }
    }
    func solvePuzzle(factorOrAddened: Int) {
        expert.move(distance: factorOrAddend * 3)
        expert.turnRight()
        expert.move(distance: factorOrAddend)
        expert.turnRight()
        for i in 1 … 2 {
            expert.move(
                distance:
                    factorOrAddend + 3)
            expert.turnLeft()
        }
        expert.turnLockUp()
        expert.turnLeft()
        for i in 1 … 2 {
            expert.move(
                distance:
                    factorOrAddend + 1)
            expert.turnRight()
        }
        expert.move(
            distance: factorOrAddend
                * 2)
        expert.collectGem()
    }
    solvePuzzle(factorOrAddend: 2)
    ```
<!-- prettier-ignore-end -->

## 後記

恭喜你成功透過參數完成目標，這用起來還不錯對吧！你已經學會了參數的使用方法，並且透過與函數的搭配簡化了程式碼。這是個很好的決定，讓我們繼續前往下一章，了解更多有關函數的任務吧！

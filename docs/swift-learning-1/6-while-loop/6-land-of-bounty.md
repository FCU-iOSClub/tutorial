# 富饒之地

挑戰：嘗試找到適合你的高效解決方案。

## 簡介

在這項挑戰中，關卡中平台的長度可能會有變化，單開關與保的排列保持不變。
你可以採取多種不同方案來通關－你能找到適合你的方案嗎？

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/6e53c455-cd79-432c-385a-541e9d41e800/public)

## 講解

無論你選擇哪種方案，都應該努力使你的代碼更有效率。這可能包括減少重複的代碼，使用更高效的算法和數據結構，以及避免無謂的計算。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

<!-- prettier-ignore-start -->
=== "基礎解答"
    ```swift linenums="1"
    func solveColumn() {
        while !isBlocked {
            if isOnClosedSwitch {
                toggleSwitch()
            } else if isOnGem {
                collectGem()
            }
            moveForward()
        }
    }
    solveColumn()
    turnRight()
    moveForward()
    turnRight()
    solveColumn()
    turnLeft()
    moveForward()
    turnLeft()
    solveColumn()
    ```
=== "進階解答"
    ```swift linenums="1"
    func solveColumn() {
        while !isBlocked {
            if isOnClosedSwitch {
                toggleSwitch()
            } else if isOnGem {
                collectGem()
            }
            moveForward()
        }
    }
    func solveAndRightTurn() {
        solveColumn()
        turnRight()
    }
    solveAndRightTurn()
    moveForward()
    solveAndRightTurn()
    turnLeft()
    moveForward()
    turnLeft()
    solveColumn()
    ```
<!-- prettier-ignore-end -->

## 後記

恭喜你完成了這一關，每個人的技能和風格都不同，因此最有效的解決方案可能因人而異。盡量適應自己的能力和風格，找到最適合你的解決方案。

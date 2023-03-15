# 向左走，向右走

挑戰：建立最有效的演算法來收集寶石和打開開關。

## 簡介

在「學習程式設計1」的最後一個挑戰中，將考驗你的演算法設計技巧。
你可以運用有許多種不同的演算法來通關，也有許多方式可以建構程式碼。

如果你沒辦法馬上想到通關方法也沒有關係！程式設計常需要對問題試盡各種方法，才能找出最有用的方式。
當你準備好後，就可以繼續學習程式設計 2。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/a116a40f-78f7-4cfc-d43c-e6de613a1b00/public)

## 講解

首先，這段代碼的主要邏輯是在一個 while 循環中，不斷地進行一些動作，直到達到特定的條件為止。
這個特定條件就是當角色到達開關時，也就是 isOnOpenSwitch 為真時，循環就會停止。

在循環中，代碼會先呼叫 moveForward() 函數，讓角色向前移動一格。然後使用 if 和 else if 條件語句進行條件判斷。
如果角色現在站在寶石上，那麼就呼叫 collectGem() 函數，撿起寶石。
然後角色向右轉，再向前移動一格，接著又呼叫 collectGem() 函數，撿起另外一個寶石。
如果角色現在站在關閉的開關上，那麼就切換開關，接著向左轉，再向前移動一格，最後再切換開關。

接下來是另一個 while 循環，這個循環會一直進行，直到角色碰到牆為止。循環中呼叫 moveForward() 函數，讓角色繼續向前移動。

最後是一個 if 條件語句，用來判斷角色右側是否被擋住。
如果右側沒有障礙物，那麼就向右轉；否則就向左轉。這樣循環就會回到最開始，角色又會繼續向前移動，直到達到開關為止。



## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
while !isOnOpenSwitch {
    moveForward()
    if isOnGem {
        collectGem()
        turnRight()
        moveForward()
        collectGem()
    } else if isOnClosedSwitch {
        toggleSwitch()
        turnLeft()
        moveForward()
        toggleSwitch()
    }
    while !isBlocked {
        moveForward()
    }
    if !isBlockedRight {
        turnRight()
    } else {
        turnLeft()
    }
}
```

## 後記

這章節展示了如何在 Swift Playground 中創建一個自動化的角色移動和互動的迷宮遊戲。
在遊戲中，角色會不斷向前移動，並且撿拾寶石、切換開關。代碼使用了 while 循環、if 條件語句、函數呼叫等基礎的 Swift 語法，讓角色能夠根據不同情況進行不同的行為。
整個遊戲流程的設計也讓人更加理解 Swift 語言中的基礎邏輯和程式設計的思維方式。

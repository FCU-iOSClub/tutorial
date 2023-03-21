# 初始化你的專家

目標：初始化一個 Expert 類型的實例，並運用 `turnLockUp()` 方法來通關。

## 簡介

這個關卡中有一個新的要件要處裡：鎖頭。若要通關，你需要轉動鎖頭，鎖頭會在一顆無法獲得的寶石前方升起一個平台。

到目前為止，你使用的角色具有一些特定的能力，比如向前走、收集寶石和切換開關，但你的角色沒有開鎖這項能力。為完成這項操作，你需要一個新的角色:專家。由於專家不會改變，你將會使用一個常數來宣告它，然後透過指定 Expert 類型對其進行初始化。

> 初始化專家
>
> let expert = Expert()

1. 初始化你的專家。
2. 讓專家四處走動，並使用點記法來下達指令。
3. 在鎖頭上使用 `turnLockUp()` 方法來顯示平台之間的路徑。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/6f94203e-eaab-44d8-3dc5-0fc2ff64e800/public)

## 講解

我們看到舞台上，有兩個寶石所在的位置，用我們之前的角色是過不去的，要首先把所在的磚塊升起來，與其他磚塊一樣平，才可以走過去。這時，我們就需要一個有特殊能力的角色“專家”，這個專家可以通過打開鎖的方式，把平台升起來，讓磚塊一樣平。

需要先定義一個角色 expert，讓它成為專家角色。

```swift
`let expert = Expert()`
```

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let expert = Expert()
func solveSide() {
    expert.moveForward()
    expert.moveForward()
    expert.moveForward()
    if expert.isOnGem {
        expert.collectGem()
    } else {
        expert.turnLockUp()
    }
}
func returnToCenter() {
    expert.turnLeft()
    expert.turnLeft()
    expert.moveForward()
    expert.moveForward()
    expert.moveForward()
    expert.turnRight()
}
for i in 1...3 {
    solveSide()
    returnToCenter()
}
solveSide()
```

## 後記

由於角色不同了，編寫的程式跟以前有很大不同，就是每個動作前都要加上角色的名字，結構是這樣的：`角色名.動作名`

ex：`expert.turnRight()`

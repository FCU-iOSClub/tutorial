# 到達階梯

目標：加入階梯來通過關卡。

## 簡介

下一個建構世界的元件是階梯。與簡單的磚塊不同，階梯需要從低到高面向正確的方向。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/2b1f2ed1-6400-4bbe-fe7c-07b59c1bca00/public)

## 講解

請記住，你可以將 .north、.south、.east 或.west 傳入 facing 參數來選擇方向。

放置階梯
將面向北方的階梯放置在座標（2，3） 處的方式如下：

```swift linenums="1"
let newstair = Stair()
world.place(newStair, facing: north,atColumn: 2, row: 3)
```
但是，還有一個捷徑可以更快速地放置階梯 ！與其單獨初始化階梯實例，不如同時初始化和放置實例。

這行程式碼可初始化並放置末命名的 Stair 類型實例：

```swift linenums="1"
world.place(Stair(), facing:north,atColumn: 1, row: 1)
```

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
world.place(Stair(), facing: south, atColumn: 3, row: 1)
world.place(Stair(), facing: south, atColumn: 3, row: 3)
world.place(Stair(), facing: west, atColumn: 1, row: 4)
world.place(Stair(), facing: west, atColumn: 1, row: 6)
world.place(Stair(), facing: east, atColumn: 5, row: 6)
world.place(Stair(), facing: north, atColumn: 2, row: 7)
world.place(Stair(), facing: north, atColumn: 4, row: 7)
func toggleSide() {
    toggleSwitch()
    while !isBlocked {
        moveForward()
        toggleSwitch()
    }
}
func turnCorner() {
    turnRight()
    move(distance: 2)
    turnLeft()
    move(distance: 2)
    turnRight()
}
move(distance: 4)
turnLeft()
move(distance: 3)
turnRight()
for i in 1...2 {
    toggleSide()
    turnCorner()
}
toggleSide()
```

## 後記

既然你試驗了放置磚塊、傳送門、開關和階梯，那麽你就掌握了建構世界的基礎。下一步，應該試著使用這些技巧來通過一些進階的世界建構關卡了。

# 浮動的島嶼

挑戰：加入磚塊、階梯和傳送門。

## 簡介

在這項挑戰中，透過加入通關所需的全部元件來練習建構世界的技巧。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/09a77d97-9020-4208-9dcc-0024d0d1f300/public)

## 講解

解決方案有很多種，你可以選擇使用傳送門來跳躍傳送，或是加入磚塊來填補缺口。

記住！！

你可以在同一行程式碼行建立和放置實例：

```swift linenums="1"
world.place(Block(), atcolumn : 2, row: 2)
```

首先，你需要初始化角色來通過關卡。看看你是否能使用虛擬碼在關卡世界中通行來想出解決方法。然後使用程式碼來改變關卡世界的架構。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let character = Character()
world.place(character, facing: south, atColumn: 1, row: 7)
func completeIsland() {
    character.toggleSwitch()
    character.jump()
    character.collectGem()
    character.turnLeft()
    character.jump()
    character.toggleSwitch()
}
completeIsland()
world.place(character, facing: north, atColumn: 6, row: 3)
completeIsland()
world.place(character, facing: east, atColumn: 1, row: 1)
completeIsland()
```

## 後記

每次找出新的解決方法後，你會更有概念，什麼解決方法適用於解決何種類型的問題。下次再遇到類似問題時，你就知道該如何解決了！

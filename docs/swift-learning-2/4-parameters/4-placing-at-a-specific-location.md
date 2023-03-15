# 置於特定位置

目標:將你的角色置於關卡世界中的特定位置。

## 簡介

到目前為止，已經為你選好角色的起點。在這個關卡中，你會透過將**引數**傳入到稱為 `place` 的**方法**來選取起點。
> `使用 place 方法`
>
> `place` 有三個**參數**：
> 
> `world.place(item: Item, atColumn: Int, row: Int)`
> 
> + **item** ：使用 `Item` 類型的輸入，包含 `Character` 和 `Expert` 類型。傳入一個專家**實例**，`expert`。
> 
> + **atColumn** ：用一個 **Int** 表示要放置角色的直欄。
> 
> + **row** ：用一個 **Int** 表示要放置角色的橫列。 
> <br> world.place (expert, atColumn: 1, row: 1)

1. 按下關卡世界中的磚塊來顯示其座標。
2. 查看地圖，為專家尋找一個起點位置。在 `place` 方法中使用該位置的直欄值和橫列值。

![img](https://ppt.cc/fddEQx)

## 講解

TODO

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
TODO()
```

## 後記

TODO

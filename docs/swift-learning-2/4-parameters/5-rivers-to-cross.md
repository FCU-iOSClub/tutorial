# 渡過河流

挑戰：將專家置於關卡世界中並且通關。

## 簡介

你現在可以將專家放置在特定位置，但如果你還想讓專家面向特定的方向呢？你可以呼叫 `place` 方法的另一種版本，就是把方向作為附加引數。
> 指定專家的方向
>
> `world.place(expert, facing: .west, atColumn: 6, row: 3)`

先等一下，`.west`是指什麼？它可以視為**點記法**的簡短形式，並能提供你一組可選用的選項。在本例中，你可以選擇 `.west` 、 `.east` 、 `.north` 或 `.south`，沒有其他選項！

類似這樣的選擇可以運作，是因為每個選項都屬於同一種**類型**，即定義一組相關值的**列舉**類型。你可以將每個選項寫成像是 `Direction.north` 這樣的形式，但也可以省略 `Direction` 以求簡潔。

首先，初始化專家。接著，在快捷鍵列中找到 `world` 並將它加入程式碼中。使用點記法來呼叫包含 `facing` 參數的 `place` **方法**，並傳入引數，然後通過關卡。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/929a9dce-c05d-4026-15aa-b26a70d02900/public)

## 講解

在這個關卡中你需要透過改變角色的面向方向，我們同樣可以透過`place`方法來解決，你只需要改變傳入的參數即可解決這個問題。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let expert = Expert()
world.place(
    expert, facing: .south,
    atColumn: 1, row: 8)
func collectGemsInLine() {
    while !expert.isBlocked {
        if expert.isOnGem {
            expert.collectGem()
        }
        expert.moveForward()
    }
}
collectGemsInLine()
expert.turnLockDown()
expert.turnLeft()
collectGemsInLine()
expert.turnLockUp()
expert.turnRight()
collectGemsInLine()
```

## 後記

太棒了，現在你知道如何透過 world 實例來存取關卡世界本身了。這項技巧將變得非常有價值，它可以讓你修改關卡世界的元件。

但你有發現解答提供的程式碼有什麼特殊之處嗎？我們在搜集寶石時加入了是否有寶石的判斷式，也許在空的方塊上搜集寶石看起來並不會怎樣，但這在實際撰寫程式時是可能會造成其他問題的，所以讓我們一起把程式做到最好吧！

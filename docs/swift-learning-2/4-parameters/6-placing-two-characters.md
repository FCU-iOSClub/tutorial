# 放置兩個角色

目標：放置一個角色和一個專家，然後使用 `jump()` 能力來通關。

## 簡介

在這個關卡中，你將為角色和專家選取起點位置，並且還需要一種新能力來通關。專家擁有開鎖的特殊技巧，而角色則擁有跳躍的特殊技巧。
> `新能力！`
>
> 當你使用以下指令時 `.Character` **類型**即擁有上下跳躍的能力：
>
> `jump()`

1. 確認角色和專家的起點位置。
2. **初始化**角色和專家並將它們置於起點位置。
3. 必要時使用 `jump()` 指令讓角色跳躍來通關。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/4e01edf9-5ef4-45c6-a002-a172e274ac00/public)

## 講解

想不到吧，在這個世界中竟然又出現了新的方塊，仔細看角色前方的那格方塊，你會發現這是個需要往上走才能前進的障礙，在以往的地圖中我們通常都會見到階梯讓你直接往上，但現在沒有了階梯，我們需要自己往上跳，所以試著使用 `jump()` 讓角色跳起來吧。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let character = Character()
let expert = Expert()
world.place(character, facing: north, atColumn: 0, row: 0)
world.place(expert, facing: north, atColumn: 3, row: 0)
func collectAndJump() {
    for i in 1...2 {
        character.collectGem()
        character.jump()
        character.jump()
    }
}
expert.toggleSwitch()
expert.turnLockUp()
collectAndJump()
character.turnRight()
collectAndJump()
character.turnLeft()
character.collectGem()
character.move(distance: 2)
character.collectGem()
```

## 後記

太出色了，將引數傳入包含參數的函數中，這很快就會成為你的常用方法。在程式設計的過程中學習新知識時，一開始可能會擔心無法掌握，但當你在不同的地方多次看到和使用這些知識後，一切都不足為懼了。程式設計得愈多，你便會對所學的概念愈加熟悉。

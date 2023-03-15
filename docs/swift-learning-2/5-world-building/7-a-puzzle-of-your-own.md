# 你自己的關卡

挑戰：改變世界中的所有元件來建立自己的關卡！

## 簡介

除了放置新的磚塊、階梯和傳送門外，你還可以加入寶石和開關。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/98562a15-42b7-433c-a767-d15735603000/public)

## 講解

加入寶石和開關
就像加入磚塊一樣，你可在 world 上使用 place 方法來放置寶石和開關。

```swift linenums="1"
world.place(Gem(), atColumn: 2, row: 3)
world.place(Switch(), atcolumn : 3, row: 4)
```

快捷鍵列中包含可在 world 實例上使用的方法。使用這些方法來建立你自己的世界：加入自己的角色、專家、寶石、傳送門等項目！請發揮你的創意，並且玩得開心！

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
world.place(Gem(), atColumn: 2, row: 3)
world.place(Switch(), atColumn: 2, row: 4)
world.removeItems(atColumn: 2, row: 3)
world.removeItems(atColumn: 3, row: 4)
```

## 後記

你可以繼續建構關卡，直到滿意為止。完成後，你甚至可以讓別人來嘗試通關！

恭喜你完成建構世界。你現在擁有能開始建構更多複雜地形的技能了！為此，你將學習如何使用陣列依照一定的順序儲存多項資訊。

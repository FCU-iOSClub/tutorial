# 依序排列

目標：將Blu、Hopper和專家依照身高排序

## 簡介

你可以使用`陣列`**類型**的一組方法，在**陣列**中加入項目或從中移除項目。
>陣列方法
>
>`remove(at: Int)`。移除**索引**中的一個項目。
>
>`append(newElement: Element)`。在陣列結尾處加入一個項目。
>
>`insert(newElement: Element, at: Int)`。在特定的索引插入一個項目。

使用**點記法**在陣列上呼叫方法。

>範例
>
>`var favoriteFoods = [🌮, 🍓, 🍣, 🍳, 🧀]`
>
>`favoriteFoods.remove(at: 2)`
>
>呼叫`remove(at: 2)`會將🍣從陣列中移除。
>
>`//[🌮, 🍓, 🍳, 🧀]`
>
>`favoriteFoods.insert(🍝,at: 1)`
>
>呼叫`insert(🍝,at: 1)`會在索引1加入🍝。
>
>`//[🌮, 🍝, 🍓, 🍳, 🧀]`

1   在下方的`characters`陣列中，移除傳送門和寶石。

2   插入一個`Expert`類型實例，使角色依照最矮在前（row 0)最高在後的順序排列。


![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/e12033ea-49b9-42ba-58aa-b8b0385a2c00/public)

## 講解

在開始解題之前，可以先看看目前的程式是如何執行，再想想如何將傳送門和寶石移除

接著再插入角色並將角色進行排序，就可以完成關卡！


## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
var characters: [Item] = [
    Character(name: .blu),
    Portal(color: .pink),
    Character(name: .byte),
    Gem(),
    Character(name: .hopper),
]
// Remove the portal
characters.remove(at: 1)
// Remove the gem
characters.remove(at: 2)
// Insert the Expert behind Byte
characters.insert(Expert(), at: 1)
var rowPlacement = 0
for character in characters {
    world.place(character, at: Coordinate(column: 1, row: rowPlacement))
    rowPlacement += 1
}
```

## 後記

你學得非常快！
掌握如何使用陣列**索引**存取和修改項目十分好用。

你還可以運用提供給你的其他**方法**來修改陣列：

removeFirst()

removeLast()

removeAll()

嘗試使用這些方法，看看它們如何運作！


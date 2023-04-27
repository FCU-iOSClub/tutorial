# 另一種建立陣列的方法

目標：建立由現有項目組成的陣列。

## 簡介

你不只可以建立陣列來放置項目，還可以依據關卡世界中現有的項目來建立陣列。

> 範例
>
> `let characters = world.existingCharacters(at: allCoordinates)`

透過上面的角色陣列，你可以反覆運算每個角色，對它們下達 `jump()` 等指令，甚至可以要求它們展示一下華麗的舞步！

> `發起動作！`
>
> 管試對角色陣列中的每個角色呼叫這些方法
>
> `danceLikeNoOneIsWatching()`
>
> `turnUp()`
>
> `breakItDown()`
>
> `grumbleGrumble()`
>
> `argh()`

在下列程式碼中，依據關卡世界中的現有角色來建立一個陣列。然後反覆運算角色陣列，讓每一個角色執行一組動作。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/6535d722-ca60-4b7d-96e1-4728f1803400/public)

## 講解

你可以使用 `world.existingCharacters(at: allCoordinates)` 來初始化現有的角色

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let allCoordinates = world.allPossibleCoordinates
for coordinate in allCoordinates {
    let height = coordinate.column + coordinate.row

    for i in 0...height {
        world.place(Block(), at: coordinate)
    }

    if height >= 8 && height < 10 {
        world.place(Character(name: .blu), at: coordinate)
    } else if height > 9 {
        world.place(Character(name: .byte), at: coordinate)
    }
}
let characters = world.existingCharacters(at: allCoordinates)
for character in characters {
    character.jump()
}
```

## 後記

表現得太好了！

在這張中你發現了各種方式來建立、使用和修改陣列。既然你的技巧已經增強，是時候將全部的知識結合再一起來建立獨特的世界，享受不同體驗了。

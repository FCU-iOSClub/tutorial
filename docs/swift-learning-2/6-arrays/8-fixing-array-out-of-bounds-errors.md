# 修正索引越界的錯誤

目標：找出索引越界的錯誤

## 簡介

你可以透過索引來存取使用陣列中的項目，就像使用任何其他變數一樣。

> 透過索引存取項目
>```swift line
> let characters = [
>   Character(name:.byte),
>   Character (name: .blu),
>   Character(name: .hopper)
> ]
>```
>
> `characters[e].toggleswitch`：Byte 切換開關
>
> `charactersr[2].jump()`：Hopper 跳躍

但是，請注意不要嘗試存取不存在的項目！這樣會造成 `索引越界錯誤` ，這種 `程式錯誤` 會導致應用程式無法執行。

> 索引越界錯誤
>
> 索引 3 處沒有項目，因此你的程式碼不會執行。
>
> `characters[3].collectGem()`

下列程式碼包含一個導致程式碼無法執行的索引越界錯誤。請找出錯誤，
加以修正，並執行稈式碼。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/7bbbf70f-6746-4ab0-8103-321f5f862e00/public)

## 講解

可以先試著跑過一次錯誤的程式碼，去判斷程式在什麼時候產生錯誤，同時可以確定索引值有沒有超過陣列的大小，並修正程式碼。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
var teamBlu: [Character] = []
// note how many characters are in your array
for i in 1...9 {
    teamBlu.append(Character(name: .blu))
}
var columnPlacement = 0
for blu in teamBlu {
    world.place(blu, at: Coordinate(column: columnPlacement, row: 4))
    columnPlacement += 1
}
// find the array out of bounds error
teamBlu[0].jump()
teamBlu[2].collectGem()
teamBlu[4].jump()
teamBlu[6].collectGem()
teamBlu[8].jump()
```

## 後記

請記住，找出程式錯誤並加以修正，是成為程式設計師不可或缺的重要部分！索引越界錯誤是導至 App 當機的常見錯誤程式之一。設計程式碼時，請隨時檢查你的程式碼，確保沒有嘗試存取陣列中不存在的部分。
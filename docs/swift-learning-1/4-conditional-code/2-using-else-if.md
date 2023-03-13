# 使用 else if

目標:使用`if`和`else if`來切換開關或收集寶石。

## 簡介

在這關中，你會發現開關跟寶石出現的地方都很隨機。

1.前往第一個隨機的磚塊處，然後加入`if`語句。
2.在你的`if`語句內加入一個`else if`區塊。
3.輸入程式碼來打開關閉的開關，如果位於寶石位置，則收集寶石。
4.重複與第二個磚塊處。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/87e81b4e-538f-46aa-dbd7-0db02bb8e000/public)

## 講解

若要知道是否該切換開關或收集寶石，請使用`if語句`來檢查一個可能的條件，以及使用`else if區塊`來檢查另一個。新的`isOnGem`條件可以幫助你判斷Byte是否位於寶石位置。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
moveForward()
if isOnClosedSwitch {}
    toggleSwitch()
} else if isOnGem {
    collectGem()
}
moveForward()
if isOnClosedSwitch {
    toggleSwitch()
} else if isOnGem {
    collectGem()
}
```

## 後記

很好！現在你知道如何編寫自己的else if語句了。

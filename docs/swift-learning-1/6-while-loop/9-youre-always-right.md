# 每次都右轉

挑戰：使用任何你喜歡的程式設計結構和模式！

## 簡介

在最後一項 while 迴圈挑戰中，請打開所有關閉的開關並收集寶石。運用你學過的技能來通關吧。

請記住，如果第一次嘗試失敗也沒關係！即使專業的程式設計者也很難一次就成功。你的目標是編寫一些程式碼，然後不斷改善，直至程式碼成功執行。祝你好運！

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/7c7fbfe1-6ae0-4e24-00c5-93c5d1c9cb00/public)

## 講解

在解決這個挑戰的過程中，你可能會遇到一些困難和挑戰，但是不要放棄。通過不斷練習和嘗試，你可以成功完成這個挑戰並提高你的編程能力。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
while !isOnGem {
    while !isBlocked {
        moveForward()
        if isOnClosedSwitch {
            toggleSwitch()
        }
    }
    turnRight()
}
collectGem()
```

## 後記

這個挑戰旨在幫助你練習不同的程式設計結構和模式。通過解決這些問題，你可以學習如何運用不同的技巧來解決問題。同時，這個挑戰也可以幫助你熟練掌握程式設計基礎，提高你的開發技能和思維能力。

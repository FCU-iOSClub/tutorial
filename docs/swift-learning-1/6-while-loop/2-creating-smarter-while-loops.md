# 建立更聰明的 While 迴圈

目標：使用 while 迴圈和 if 語句來打開所有開關。

## 簡介

現在試試看使用條件碼來更聰明地製作你的 while 迴圈。為了通關，你需要 while 迴圈來打開三個平臺上的每一個開關。不過，你不能只使用條件 `isOnClosedSwitch`，否則迴圈會在你抵達傳送門或打開開關時停止執行。

1. 選取快捷建列中的 `while` 來加入 while 迴圈。
2. 加入條件來讓角色繼續前進，直到抵達第三個平臺的盡頭。
3. 在你的 while 迴圈中，使用 if 語句來只打開關閉的開關，而不關掉打開的開關。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/df15c191-4332-4c3d-4dd0-27455fef7100/public)

## 講解

這題可以先決定如何透過 while 語句走到盡頭，並在思考如何透過 if 語句來打開關閉的開關。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
while !isBlocked {
    if isOnClosedSwitch {
        toggleSwitch()
    }
    moveForward()
}
```

## 後記

通過這個練習，您已經學會如何使用 while 迴圈和 if 語句來處理多個開關的狀態。但是，這只是 Swift 程式的冰山一角。還有很多其他的控制結構和語法可以讓您更好地編寫 Swift 。

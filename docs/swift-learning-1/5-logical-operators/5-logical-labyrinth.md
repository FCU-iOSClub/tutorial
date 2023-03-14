# TODO

挑戰：使用邏輯運算子和條件碼來在關卡世界中通行。

## 簡介

運用先前學習過的運算子來通關吧。

* NOT 運算子 (！) 如果「不是」此條件，就這麼做。
* AND 運算子 （&&） 只有在兩者「皆」為真時才會執行程式碼。
* OR 運算子 （||） 在其中「至少」一個為真時執行程式碼。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/b4c26d63-4c83-49b2-2bfa-6237daba5f00/public)

## 講解

運用之前練習過的指令來通關吧！這個挑戰比較具有挑戰性，如果你覺得困難別放棄，可以先多思考、觀察一下。完成這一關就達成了邏輯運算子的里程碑囉！

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
for i in 1 ... 8 {
    moveForward()
    if isOnGem && isOnClosedSwitch {
        turnRight()
        moveForward()
        moveForward()
        collectGem()
        turnLeft()
        turnLeft()
        moveForward()
        moveForward()
        turnRight()
        collectGem()
        toggleSwitch()
    } else if isOnClosedSwitch {
        turnLeft()
        toggleSwitch()
    }
    if isOnGem {
        collectGem()
    }
}
```

## 後記

你真的太棒了！這些關卡可能會讓你感到挑戰，但是不要放棄！繼續嘗試並思考每個問題的解決方案。當你解決了一個問題，你應該感到自豪，因為這代表著你的進步和成就。如果你遇到困難，請不要擔心，因為挑戰是學習的一部分。試著思考不同的方法和解決方案，你會發現你有更多的能力和創造力。最重要的是，要享受這個過程！學習編寫程式是一個令人興奮和具有挑戰性的旅程，在這個過程中你會獲得許多技能和知識。繼續努力，相信自己，你會成為一名優秀的程式設計師！

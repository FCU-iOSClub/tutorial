# 拓展技能

挑戰：將重複的模式分解成函數和 for 迴圈。

## 簡介

同學們已經學習了程式設計的基礎知識，並使用你的角色通過了許多關卡。既然你已瞭解了指令、函數和 for 迥圈，那麼你一定準備好運用各種技能來完成這項挑戰了！

在關卡世界中一共有三段階梯，每段階梯都包含一組相同的任務需要執行。你能參透這些任務的模式並寫出程式碼嗎？

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/7ece953d-11da-432e-e27a-c9b263ee5200/public)

## 講解

同學們可以針對此關卡中要爬上去的每段階梯編寫函數，讓你的角色走到階梯盡頭，切換開關，然後再走回下方。

可以使用 for 迴圈重複一組動作來完成每段階梯。

嘗試解決第一段階梯，然後使用迴圈來重複同一組動作，解決其他兩段階梯。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func traverseStairway() {
    for i in 1...7 {
        moveForward()
    }
}
func clearStairway() {
    traverseStairway()
    toggleSwitch()
    turnRight()
    turnRight()
    traverseStairway()
    turnRight()
}
for i in 1...3 {
    moveForward()
    moveForward()
    turnRight()
    clearStairway()
}
```

## 後記

做得好！你很努力才來到這裡。把問題分解成容易解決的較小部分，再將處理小部分的解決方法組合成一個解決大問題的方法，這是一個不錯的解題方式。

# 全面而撤體

挑戰：辦識重複的模式並定義一個函數。

## 簡介

在這項挑戰中，你需要收集許多寶石。事實上，數量多到可以透過多種方式來通過關卡。

選取一條重複某種模式的路線，並且在你的函數中使用該模式。

如果你的程式碼第一次執行不成功，請持續嘗試，畢竟熟能生巧！（但一如往常，準備好之後，你也可以繼續前往下一關。）

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/21cb5f5e-a2f6-4504-331b-9cacc69b8900/public)

## 講解

這題不會只有一種寫法，活用你在之前的關卡中學到的知識，並且多方嘗試！

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func collectTwoGems() {
    collectGem()
    moveForward()
    collectGem()
    moveForward()
    turnRight()
}
collectTwoGems()
collectTwoGems()
collectTwoGems()
collectGem()
moveForward()
turnRight()
collectTwoGems()
```

## 後記

如果你成功解決了這一關，不妨再多想一下，有沒有辦法用更簡潔的方式來完成這一關呢？

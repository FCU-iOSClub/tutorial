# 兩個專家

挑戰：運用初始化、**參數**以及你的程式設計工具箱中其他技巧的知識來通過關卡。

## 簡介

若要完成這項挑戰，你需要兩個專家一起合作。它們需要各自打開不同的鎖頭來升起和降下不同的平台，以便收集寶石。

還記得**類型**只是實例的藍圖嗎？你可以**初始化**相同類型的兩個實例。它們基本上一模一樣，但你可對它們進行個別的控制。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/83af3e53-4ed4-4ed9-7359-3db7372b6700/public)

## 講解

在先前的關卡中我們會建立一個角色跟一個專家的實例，那如果我想建立兩個專家實例呢？你只需要用不同的名稱來創建實例就可以囉！

`let character = Character()` 還記得這段程式碼吧！接在 `let` 後方以小寫開頭的就是該實例的名稱，將其改變就能夠創建不同的實例了！

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let topExpert = Expert()
let bottomExpert = Expert()
world.place(topExpert, facing: north, atColumn: 0, row: 4)
world.place(bottomExpert, facing: east, atColumn: 0, row: 0)
bottomExpert.collectGem()
bottomExpert.move(distance: 3)
bottomExpert.turnLeft()
bottomExpert.turnLock(up: true, numberOfTimes: 2)
bottomExpert.turnRight()
topExpert.turnLockDown()
bottomExpert.move(distance: 3)
bottomExpert.turnLock(up: false, numberOfTimes: 2)
topExpert.turnRight()
while !topExpert.isBlocked {
    if topExpert.isOnGem {
        topExpert.collectGem()
    }
    topExpert.moveForward()
}
```

## 後記

Amazing! 當你使用類型 (例如 Expert) 時，你就可以建立許多該類型的實例。由於它們都來自相同的藍圖，你可以呼叫同一個方法來存取該類型任意實例上的相同屬性。

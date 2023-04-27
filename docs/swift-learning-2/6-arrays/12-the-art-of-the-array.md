# 陣列的藝術

挑戰：使用角色陣列來創作舞蹈表演。

## 簡介

在編寫自己的程式碼這方面，你已經得到了很大的進展。現在應該要開讀和修改一些現有的程式碼了！

> 範例
>```swift
> //這是一條程式碼註解。App 不會執行它，因此你可以隨意編寫！
>```

註解是用來幫助你組織程式碼和記錄每個部分的内容。下列程式碼中的註解可以幫助你閱讀和理解每段程式碼的功用。

1. 嘗試針對下列現有的程式碼進行修改和加入，創作出你喜歡的舞蹈表演。
2. 隨意修改，並加入一些亮點讓程式碼具有個人特色

請記住，這裡沒有錯誤的答案!

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/a91b9191-6a68-470d-08c7-9d74f60f5800/public)

## 講解

註解對於程式設計師來說是一個極為重要的部分，讓其他人可以更容易理解你的程式碼，自己再重新閱讀程式碼時也可以輕鬆許多。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
// Create coordinate zones.
let allCoordinates = world.allPossibleCoordinates
let backRow = world.coordinates(inRows: [9])
let insideSquare = world.coordinates(inColumns: [4, 5], intersectingRows: [4, 5])
let squareCorners = world.coordinates(inColumns: [2, 3, 6, 7], intersectingRows: [3, 7])
// Place platform locks.
let squareLock = PlatformLock(color: .green)
world.place(squareLock, at: Coordinate(column: 1, row: 1))
let cornerLock = PlatformLock(color: .pink)
world.place(cornerLock, at: Coordinate(column: 8, row: 1))
let backLock = PlatformLock(color: .blue)
world.place(backLock, at: Coordinate(column: 4, row: 1))
// Place characters and platforms.
for coor in insideSquare {
    world.place(Platform(onLevel: 4, controlledBy: squareLock), at: coor)
    world.place(Character(name: .hopper), at: coor)
}
for coor in squareCorners {
    world.place(Platform(onLevel: 4, controlledBy: cornerLock), at: coor)
    world.place(Expert(), at: coor)
}
for coor in backRow {
    world.place(
        Platform(onLevel: 2, controlledBy: backLock),
        at: Coordinate(
            column:
                coor.column, row: coor.row + 1))
    world.place(Character(name: .blu), facing: north, at: coor)
}
// Create arrays from existing characters.
let blus = world.existingCharacters(at: backRow)
let hoppers = world.existingCharacters(at: insideSquare)
let experts = world.existingExperts(at: squareCorners)
// Do cool stuff.
squareLock.movePlatforms(up: true, numberOfTimes: 3)
for hopper in hoppers {
    hopper.turnUp()
}
cornerLock.movePlatforms(up: true, numberOfTimes: 7)
for expert in experts {
    expert.collectGem()
}
for blu in blus {
    blu.jump()
}
backLock.movePlatforms(up: true, numberOfTimes: 11)
for blu in blus {
    blu.jump()
}
```

## 後記

太神奇了！對於程式設計師來說，閱讀和調整現有程式碼的能力極為重要。很多時候你都需要去理解其他人的程式碼。將來，你會開始寫自己的程式碼註解，讓你的程式碼更清楚，其他人也能理解。

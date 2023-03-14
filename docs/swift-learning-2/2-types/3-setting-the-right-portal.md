## 設定正確的傳送門

目標：修改每個傳送門的狀態來收集寶石。

## 簡介

這一關有兩個傳送門，你需要使用這兩個傳送門，讓角色到達關卡世界中的其他部分。但由於你還需要走過一些區域，因此在修改 isActive 屬性時必須分別引用每個傳送門實例。
為此，你必須設定每個傳送門實例的狀態。狀態是任何指定時間内變數所儲存的資訊。因此，傅送門實例儲存的 isActive 值有時為true，有時為 false。

1. 規劃如何打開和關閉每個傳送門來收集所有寶石。
2. 使用點記法在通關過程中修改 bluePortal 和 pinkPortal 的 isActive 屬性。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/f310438a-4cc1-4092-27ad-2e52f5385700/public)

## 講解

首先，讓你的角色穿過藍色傳送門，到達傳送門另一頭的寶石處。你可能需要關閉藍色傳送門才能取得兩顆寶石。關閉粉紅色的傳送門，讓你的角色可以到達其後方的寶石處。然後再重新打開傳送門以傳送到最後一顆寶石處。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
func moveCollect() {
    moveForward()
    collectGem()
}
func turnAround() {
    turnLeft()
    turnLeft()
}
moveForward()
moveCollect()
turnAround()
bluePortal.isActive = false
moveForward()
moveCollect()
turnAround()
bluePortal.isActive = true
pinkPortal.isActive = false
moveForward()
moveForward()
moveForward()
collectGem()
turnAround()
pinkPortal.isActive = true
moveForward()
turnAround()
moveCollect()
```

## 後記

按照傳送門的實例名稱對每個傳送門進行參照後，你可以控制關卡世界的特定元件。隨著你程式設計工具箱中的技巧不斷增加，你會慢慢發現這個技巧的實用性有多大。

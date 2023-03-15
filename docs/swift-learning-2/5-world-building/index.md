# 建構世界

在前面的關卡中我們學到了如何初始化及使用我的專家，而在建構世界關卡中，你可以使用程式碼，改變你身處的世界。你要做的，只是描述一下想要構造的東西和放置的位置。

## 範例：初始化寶石

在一張 Playgrounds 中，我們常需要 moveForward 去 collectGem 或 toggleSwitch ，但如果有一張地圖的並沒有寶石在地上但又要我們去撿的話該怎麼辦？

其實我們只要先初始化出我們的寶石就行了。

下列程式碼為先初始化寶石並在 world 中放置。
```swift linenums="1"
    let gem = Gem ()
    world.place ()
```
雖然我放置了寶石，但 swift 並不知道我是要放在哪一個地方，所以我還需要加座標值。

place 方法有三個參數：

.item 採用了 Item 類型的輸入（如磚塊、寶石或階梯）

.atColumn 和.row 採用了Int 值，指示項目放置的位置

```swift linenums="1"
    world.place(item: Item, atColumn: Int, row: Int)
```


呼叫 place 方法時，會傳入gem 以及要放置gem 的位置座標，例如：

```swift linenums="1"
    world.place(gem, atColumn: 5, row: 1)
```
這方法也可以適用在放方塊、開關或角色等

如果你像移除項目則可以用 world.removeItems 的方法

```swift linenums="1"
    world.removeItems(gem, atColumn: 5, row: 1)
```

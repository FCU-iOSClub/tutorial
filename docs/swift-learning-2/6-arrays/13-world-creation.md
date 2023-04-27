# 創造世界

挑戰：創意無極限！

## 簡介

在「學習程式設計 2」的最後一項挑戰中，你可以自由發揮創意！空白的程式碼區域可能會讓人有些害怕，如果想要在此使用其他頁面的程式碼，請随意拷貝和貼上！

你可以嘗試下列的一些想法：
- 使用陣列來建造一座高樓，並將 Byte 放在樓頂、
- 建造一個到處都是傅送門的世界。然後將一個角色陣列放置在世界中，讓各個角色在傅送門之間穿楼。
- 創造一場表演，並讓你的角色透過它們的行為相互溝通。
- 建立一個關卡，讓其他人嘗試通關。

你還有其他想法嗎？當然如此！程式設計極具創造性，因此請讓你的想像力盡情飛馳，編寫你想要的程式碼！

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/3dc2d740-ab8a-4f5e-08d5-03eb9929c300/blue)

## 講解

如果沒有想法的話可以試著從過去的關卡中去修改，或是融合兩個不一樣的關卡，祝你順利～

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
for coordinate in world.row(7) {
    world.place(Character(name: .blu), at: coordinate)
}
for coordinate in world.row(5) {
    world.place(Character(name: .byte), at: coordinate)
}
for coordinate in world.row(3) {
    world.place(Character(name: .hopper), at: coordinate)
}
```

## 後記

棒極了！

你完成「學習程式設計2」，慶祝一下吧！這可是一想了不起的成就。但這並不是旅程的終點，而只是開始。學習程式設計如同學習語言，你需要多加練習，才能更為熟練。嘗試在較早的關卡中使用你的新技巧，看看能否運用進階的解決方式成功通關。或是加把勁，嘗試一下 Blu 的冒險和一些程式設計的挑戰。不管你選擇進行哪一種練習，請努力達成標並持續進行程式設計吧！

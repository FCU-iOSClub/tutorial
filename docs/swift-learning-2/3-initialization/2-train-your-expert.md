# 訓練你的專家

目標：建立一個 Expert 類型的實例，並使用專家來通關。

## 簡介

運用這項挑戰來練習初始化專家實例。在編寫關卡的解決方法時，請想想你所學到的關於將程式碼分解成清楚、可重複使用函數的相關知識。

新能力
除了 `turnLockUp()` 外，你還可以使用 `turnLockDown()` 將平台從目前的位置往下移。

首先，初始化一個專家實例。引導你的專家四處走動，收集寶石，並且轉動鎖頭來顯示通往中斷平台的路徑。


![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/0a2006a7-2964-4b91-c5b1-e0595cebc900/public)

## 講解

這裡增加了一個向下轉鎖的操作，就是把平台下降後，可以走過去收集寶石。
還是先要初始化專家的屬性：`let expert = Expert()`

然後我們創建一個變量 gemCounter 用來給寶石計數。

` var gemCounter = 0`

接下來，我們定義收集寶石的函數 `moveAndCollect()`：

* 向前走
* 如果是寶石，收集寶石，寶石數量 + 1
* 如果寶石數量是3，且前方受限，那麼向下轉動鎖
* 如果前方受限，轉身
* 如果左右都不受限，右轉

然後我們使用定義好的函數，使用 while 循環，直到寶石數量到6。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let expert = Expert()
func turnAround() {
    expert.turnLeft()
    expert.turnLeft()
    expert.moveForward()
    expert.moveForward()
}
func completeSide() {
    expert.moveForward()
    expert.moveForward()
    expert.collectGem()
}
for i in 1...2 {
    completeSide()
    turnAround()
    expert.turnRight()
}
completeSide()
expert.turnLockDown()
turnAround()
expert.turnRight()
for i in 1...3 {
    expert.moveForward()
}
expert.turnLeft()
for i in 1...3 {
    completeSide()
    turnAround()
    expert.turnLeft()
}
```

## 後記

新增了新的動作指令，讓學員以更複雜的命令指示專家完成任務。

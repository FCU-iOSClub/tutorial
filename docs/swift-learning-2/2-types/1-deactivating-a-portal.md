# 關閉傳送門

目標：關閉傳送門來到達開關處。

## 簡介

你到目前為止一直使用 moveForward(）或 turnleft（)，以一般的方式呼叫函數。這些函數可用來讓角色四處走動，但你無法將它們用於關卡世界中的其他項目，例如，傳送門。
若要關閉傳送門，你將使用點記法來更改特定傳送門實例的isActive 屬性。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/adc39d41-68a4-444c-29f4-a10d17768900/public)

## 講解

1.使用點記法將 greenPortal 實例的 isActive 屬性設為false。
2.打開每個開關。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
greenPortal.isActive = false
func moveThree() {
    moveForward()
    moveForward()
    moveForward()
}
for i in 1...3 {
    moveThree()
    turnRight()
    moveThree()
    toggleSwitch()
    turnLeft()
    turnLeft()
}
```

## 後記

你可以使用點記法來修改特定實例的屬性。首先，參照實例名稱（例如 greenPortal），然後加上句點（.）和要修改的屬性。準備好繼續了嗎？

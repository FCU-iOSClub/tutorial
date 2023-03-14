# 需要兩個人合作

目標：建立 Character 和 Expert 類型的實例並讓它們合作通關。

## 簡介

在這項挑戰中，你需要初始化你的角色和專家實例，然後使用它們兩個來通過關卡。但你器要結合兩者的動作來讓它們共同合作，而非一次只集中在一個實例上。

首先，建立一個角色實例和一個專家實例。使用專家來轉動其中一個鎖頭，讓角色能夠到達實石或開關處。然後打開另外一個鎖頭，以便角色能夠完成挑戰。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/57cdc9e7-17f8-4c51-b266-33e9f7b04700/public)

## 講解

1. 定義兩個角色，然後建立3個變數，用於計數。
2. 一個計算收集寶石的數量，一個計算打開開關的數量，一個計算 expert 前進的步數。
3. 初始化角色，建立變數。
4. 最後是主程序，expert 走5步，轉動綠色鎖，降下綠色平台。
5. expert 走15步，轉動紫色鎖，升起紫色平台。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let expert = Expert()
let character = Character()
func turnCorner() {
    expert.moveForward()
    expert.moveForward()
    expert.turnRight()
    expert.moveForward()
    expert.moveForward()
}
expert.turnLeft()
expert.moveForward()
turnCorner()
expert.turnLeft()
expert.turnLockDown()
expert.turnLockDown()
character.moveForward()
character.moveForward()
character.collectGem()
expert.turnRight()
turnCorner()
expert.moveForward()
expert.moveForward()
turnCorner()
expert.turnLeft()
expert.turnLockUp()
character.moveForward()
character.moveForward()
character.toggleSwitch()
```

## 後記

這一關不同的地方在於，兩個平台是由兩個鎖分別控制的，綠色的平台由綠色的鎖控制，紫色的平台由紫色的鎖控制。

開發沒有難度，主要還是區分兩個角色的動作，要分別在動作前面加上名字的前綴，才能分清楚，是哪個角色去做動作。
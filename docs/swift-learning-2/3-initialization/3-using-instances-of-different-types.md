# 使用不同類型的實例

目標：初始化一個 Expert 類型的實例和一個 Character 類型的實例。

## 簡介

在編寫程式碼時，常常會同時使用多個實例和元件來解決較大的問题。例如，若你要建構一個照片編輯 App，你需要使用相機來拍攝影像，使用濾鏡資料庫來套用有趣的效果。

在這個關卡中，你需要專家的開鎖能力來幫助你的角色通過傳送門，然後到達遠處平台上的寶石處。

1. 建立一個 Expert 類型的實例和一個 Character 類型的實例。
2. 讓專家轉動鎖頭。
3. 讓角色使用傳送門並收集兩顆寶石。

![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/e6efc883-fda4-4e6e-85ae-ec82648e1f00/public)

## 講解

使用不同類型的實例

首先要定義兩個人物，一個專家，一個普通角色

> `let expert = Expert()`
>
> `let character = Character()`

這裡需要兩個人物互相配合，開始的時候，專家先升起平台，character 收集完第一顆寶石後，走到傳送門，然後，專家再降下平台，character 去收集第二顆寶石。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let expert = Expert()
let character = Character()
expert.moveForward()
expert.turnLockUp()
character.moveForward()
character.collectGem()
character.moveForward()
character.turnRight()
character.moveForward()
character.moveForward()
expert.turnLockDown()
expert.turnLockDown()
character.moveForward()
character.collectGem()
```

## 後記

讓學員練習一次操控多個角色去完成關卡任務。

# 除錯練習

挑戰：調整指令順序來排除程式碼的錯誤。

## 簡介

在這項挑戰中，你將練習發現程式錯誤的技巧，找出下方程式碼中順序錯亂的指令並且重新排序。

<!-- prettier-ignore -->
!!! info "注意"
    注意這張地圖上有一個開關一開始就是打開狀態。如果 Byte 將這個開關切換成關閉狀態，就會導致程式錯誤。你需要打開所有開關來完成這項挑戰。

最好在每次更動後都執行一次程式碼，以確認你已經找出並修正每個程式錯誤。不用擔心嘗試的次數太多。犯錯是學習和牢記新知識的一種絕佳方式！

![bug-squash-practice](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/89c06321-a7dd-4278-d20b-daf7ade7e800/public)

## 講解

跟上一關一樣，你需要對現有的程式碼進行修改，並且將指令重新排序，以便完成挑戰。

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
moveForward()
turnLeft()
moveForward()
moveForward()
toggleSwitch()
moveForward()
moveForward()
moveForward()
moveForward()
collectGem()
```

## 後記

相信你的除錯能力已經更上一層樓，下一關就是指令章節的最後一章了，繼續努力！

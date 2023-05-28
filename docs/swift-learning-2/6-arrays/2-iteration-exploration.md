# 探索反覆運算

挑戰：反覆運算陣列，在各個位置放置寶石和開關

## 簡介

在下方程式碼中，你可以使用`columns`**陣列**來在關卡世界中的每個直欄放置寶石和開關。此過程叫做**反覆運算**，它可以讓你在陣列中為每個項目執行動作。

>範例
>
>若要反覆運算，請使用 for-in 迴圈，它是一種**for迴圈**的類型
>
>```
>for currentColumn in colums {
>   world.place(Gem(),atColumn:currentColumn , row:1)
>}
>```
`for-in`迴圈中會在陣列中替每個**變數**執行程式碼區塊。在上方範例中，`currentColumn`是儲存`columns`陣列中數值的變數。此數值會傳遞到`place`方法的`column`**參數**，以決定要放置寶石的直欄。

每次`for-in`迴圈執行時，`currentColumn`會前往陣列中的下一個項目，直到沒有剩下的項目。

1   完成會在陣列中反覆運算的的`for`迴圈。

2 	在迴圈中，在每個直欄放置寶石和開關。


![img](https://imagedelivery.net/cdkaXPuFls5qlrh3GM4hfA/ff0fc349-2ee3-4ad4-7aa5-4df7baf76800/public)

## 講解

試著在迴圈中放置寶石和開關，就能輕鬆完成任務了！

## 解答

--8<-- "docs/snippets/danger-do-it-yourself.txt"

```swift linenums="1"
let columns = [0, 1, 2, 3, 4]
for currentColumn in columns {
    world.place(Gem(), atColumn: currentColumn, row: 1)
    world.place(Switch(), atColumn: currentColumn, row: 1)
}
```

## 後記

現在你學會反覆運算了！

採用**反覆運算**陣列的方式來建構世界，比一次只放置一個項目要快得多。若要反覆運算陣列，請使用for-in 迴圈為陣列中的每個項目執行動作

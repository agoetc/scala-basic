値同士を比較することができます。  
結果は真偽型(Boolean型)です。  
正しい場合は**true**  
正しくない場合は**false**  
という風に評価されます。  
文では分かりづらいと思うので実際にコードを見てみましょう。  
```scala
// イコール
println(1 == 1)
> true

// ノットイコール
println(1 != 1)
> false

// 大なり
println(1 > 2)
> false

// 大なりイコール
println(2 >= 2)
> true

// 小なり
println(1 < 3)
> true

// 小なりイコール
println(1 < 3)
> true
```


また、真偽型も文字列型や数値型と同じように変数に入れることができます。
```scala
// この2つは同じ結果になる
val hoge: Boolean = true
val hoge: Boolean = 1 == 1

// もちろん型を省略することができる
val hoge = false
```

!!! tip
    `=`は変数の代入です。  
    比較は`==`です。  
    本当によく間違えるので注意しましょう。


## 複数条件
`&&`(AND)や`||`(OR)で比較を連結することで、  
同時に複数の比較をすることが出来ます。  
```scala
val age = 18
val height = 150

// ageが18以上かつheightが160以上ならtrue
println(age >= 18 && height >= 160)
> false

// ageが18以上またはheightが160以上ならtrue
println(age >= 18 || height >= 160)
> true
```

真偽型の使い方は次ページにて説明します。  
次ページから少し複雑になってきますが頑張ってください。

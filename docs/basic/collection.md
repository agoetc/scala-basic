コレクション型の紹介をします。  
コレクション型はいっぱいあるんですが、  
本サイトでは2種類しか紹介しません。  
## List型
複数の値を入れることが出来る箱です。  
```scala
val numbers: List[Int] = List[Int](1, 2, 3)

// 型を省略した書き方
val numbers = List(1, 2, 3)

println(numbers)
> List(1, 2 ,3)
```

コレクションには1種類の型しかいれることが出来ません。  
なので、Int型のListを作成する場合は`List[Int]`、  
String型のListを作成する場合は`List[String]`と宣言しましょう。  
ですが型推論があるので宣言しなくてもいいです。

### 値を取得する
Listに入れたものを使用します。  
コレクションは、0番目、1番目、2番目といった数え方をします。

下記コードで`println(alphabets(0))`で`"A"`が出力されているのはそのためです。
```scala
val alphabets = List("A", "B", "C")  
println(alphabets(0))
> "A"

println(alphabets(1))
> "B"

// 10個目の値を取り出そうとするが、存在しないのでエラー
println(alphabets(9))
```


### 値を追加する
`:+`にて値を後ろに、`+:`で先頭に追加することが出来ます。  
また、`++`でList同士を結合することが出来ます。
```scala
val alphabets = List("A", "B", "C")

// 一番後ろに追加
val newAlphabets = alphabets :+ "D"
println(newAlphabets)
> List("A", "B", "C", "D")

// 一番前に追加
val newAlphabets = "D" +: alphabets
println(newAlphabets)
> List("D", "A", "B", "C")

// List同士の合成
val newAlphabets = alphabets ++ List("D", "E")
println(newAlphabets)
> List("A", "B", "C", "D", "E")
```


## Map型
Listでは0番目、1番目、2番目といった数え方で  
`list(0)`のように何番目か指定して取得していましたが、  
Mapでは対応するキーに応じたものを収納・取得することが出来ます。  
```scala
val menu: Map[String, Int] = Map[String, Int]("apple" -> 100, "orange" -> 50, "banana" -> 120)

// 型を省略した書き方
val menu = Map("apple" -> 100, "orange" -> 50, "banana" -> 120)

println(menu)
> Map(apple -> 100, orange -> 50, banana -> 120)
```


### 値を取得する
Mapに入れたものを使用するには。  
Mapを宣言したときに入れた、左側の値を渡してあげます。
```scala
val menu = Map("apple" -> 100, "orange" -> 50, "banana" -> 120)

println(menu("apple"))
> 100

println(menu("orange"))
> 50

// mangoを取り出そうとするが、存在しないのでエラー
println(menu("mango"))
```


### 値を追加する
`++`でMap同士を結合します。
```scala
val menu = Map("apple" -> 100, "orange" -> 50, "banana" -> 120)

val newMenu = menu ++ Map("mango" -> 200)
println(newMenu)
> Map(apple -> 100, orange -> 50, banana -> 120, mango -> 200)
```


このページではコレクションを紹介しましたが、  
存在しない値を取得するときにエラーが出てしまって危ないですよね。  
次ページではこうした危険を回避する最高な機能を紹介します。

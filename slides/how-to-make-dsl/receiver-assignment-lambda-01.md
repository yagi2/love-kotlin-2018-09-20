## レシーバ指定のラムダ式
<br />
ラムダ式にレシーバーを指定して、ラムダ式の中のスコープの`this`をそのクラスにする機能。
  
```Kotlin
data class Fruit(val name: String, val num: Int)

fun hoge(lambda: Fruit.() -> Unit) {
  val apple = Fruit("りんご", 10)
  apple.lambda()
}

hoge {
  // ここのthisはFruitになっている
  println("${this.name}が${this.num}個あります。") // -> りんごが10個あります。
  
  // もちろんthisは省略可能
  println("${name}が${num}個あります。") // -> りんごが10個あります。
}
```
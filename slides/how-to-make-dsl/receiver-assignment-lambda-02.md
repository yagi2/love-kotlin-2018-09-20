## レシーバ指定のラムダ式
<br />
スコープの関数のwith
  
```Kotlin
fun <T, R> with(receiver: T, block: T.() -> R): R { ... }
```  
  
第1引数でTクラスを受け取り、そのTクラスを指定したラムダ式を第2引数で受け取る。
  
```Kotlin
data class Fruit(val name: String, val num: Int)

val apple = Fruit("りんご", 10)
with(apple) {
  // apple(Fruitクラス)を渡しているので、ここのthisはFruit
  println("${name}が${num}個欲しい！") // -> りんごが10個欲しい！
}
```
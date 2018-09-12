## 中置関数
<br />
メソッド呼び出し時に`.`を使わずにスペースで挟むこと（中置にすること）で呼び出せるようになる。
`infix`をつけたメソッドが中置関数となる。  

```Kotlin
"a" to "b" // -> Pair<String, String>
```
<br />
これは`Tuples.kt`に実装がある
  
```Kotlin
public infix fun <A, B> A.to(that: B): Pair<A, B> = Pair(this, that)
```

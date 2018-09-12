## 中置関数
<br />
長澤太郎さんが作られているJUnitをシンプルに書けるライブラリ  
<a href="https://github.com/ngsw-taro/knit/" target="_blank">ngsw-taro/knit: JUnit API set for Kotlin</a>での例  

```Kotlin
val actual = "hoge"
val expected = "hoge"

actual.should be expected
```

`be`が中置関数になっている。  
  
```Kotlin
interface Asserter<T> {
    infix fun be(expected: T)
}

internal class AsserterImpl<T>(override val target: T) : Asserter<T> {
    override fun be(expected T) {
        target.should(`is`(expected))
    }
}
```
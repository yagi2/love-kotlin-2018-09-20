## 拡張関数・拡張プロパティ
<br />
既存のクラスに新しいメソッドやプロパティを生やすことが出来る。  
  
```Kotlin
fun String.toPackedString() =
    this.replace("\n", "").replace(" ", "")

"""
{
    "name": "yagi2",
    "age": 24
}
""".toPackedString() // -> "{"name":"yagi2","age":24}"

var <T> List<T>.lastIndex: Int
    get() = size - 1

listOf(1, 2, 3).lastIndex // -> 2
```
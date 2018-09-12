## メソッドの引数の最後がラムダ式であれば<br />外側に出せる
<br />
  
```Kotlin
fun hoge(num: Int, lambd: () -> String)

hoge(100, { "this is lambda" })
hoge(100) { "this is lambda" }

fun piyo(lambda: () -> String)
piyo({ "this is lambda "})
piyo {
  "this is lambda"
}
```

ちょっとDSLっぽい見た目になる。
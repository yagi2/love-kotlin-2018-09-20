## `@DslMarker`アノテーション
<br />
プロックが入れ子になった際に、内側のブロックから外側のブロックにアクセスできるようになってしまうのが多々ある。  
それを防ぐためのアノテーション。  
  
具体的には以下のようなケースを防ぐことが出来る。  
  
```Kotlin
html {
    head {
        // headの中のthisがthis@htmlになっている、this@headになってほしい
        head {　}
    }
}
```
 　
<a href="https://github.com/Kotlin/KEEP/blob/master/proposals/scope-control-for-implicit-receivers.md" target="_blank">KEEP/scope-control-for-implicit-receivers.md at master · Kotlin/KEEP</a>  
<a href="https://github.com/Kotlin/kotlinx.html/blob/dsl-markers/DSL-markers.md" target="_blank">kotlinx.html/DSL-markers.md at dsl-markers · Kotlin/kotlinx.html</a>  
<a href="https://blog.jetbrains.com/kotlin/2016/11/kotlin-1-1-m03-is-here/" target="_blank">Kotlin 1.1-M03 is here! | Kotlin Blog</a>  
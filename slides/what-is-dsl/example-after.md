# Kotlin DSL  
DSLは構造と文法を持つ。

DSLを用いたケース
```Kotlin
val html = createHtml().
    table {
        tr {
            td {
                + "セルです。"
            }
        }
    }
```
  
ぱっと見の明らかなわかりやすさ😤  
<a href="https://github.com/Kotlin/kotlinx.html" target="_blank">Kotlin/kotlinx.html: Kotlin DSL for HTML</a>
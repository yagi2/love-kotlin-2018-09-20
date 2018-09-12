# Kotlin DSL Example   
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
  
<br />
ぱっと見の圧倒的わかりやすさ😤  
<a href="https://github.com/Kotlin/kotlinx.html" target="_blank">Kotlin/kotlinx.html: Kotlin DSL for HTML</a>
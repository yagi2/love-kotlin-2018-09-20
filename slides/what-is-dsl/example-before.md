# Kotlin DSL  
DSLは構造と文法を持つ。

普通に書いたケース
```Kotlin
val html = createHtml()
val table = createTable()

html.addChild(table)

val tr = createTr()
table.addChild(tr)

val td = createTd()
tr.addChild(td)

td.text = "セルです"
```
<img src="img/anko-logo.png" width=45% />  
Ankoという、Androidアプリを制作を快適にするライブラリがある  
その中に`Anko Layout`というDSLでレイアウトを組めるものがある  
  
```Kotlin
linearLayout {
    padding = dip(30)
    
    textView {
        text = "A"
    }.lparams {
        margin = dip(30)
    }
}
```

<a href="https://github.com/Kotlin/anko" target="_blank">Kotlin/anko: Pleasant Android application development</a>
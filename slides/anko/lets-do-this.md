## 実際に作ってみる  
AnkoのようなDSLでレイアウトをビルドするようなものを作ってみる  
（とりあえず汎用性は無視）  
<br />
（時間がありそうならライブコーディングで作ります）  
  
目指す完成形  
  
```Kotlin
linearLayout {
    textView {
        text = "Hello,"
        textColor = Color.RED
    }.lparams {
        margin = dip(10)
    }
}
```

`LinearLayout`と`TextView`を作れて`LayoutParams`も指定できるような。 

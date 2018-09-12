## 演算子オーバーロード
<br />
Kotlinでは既に用意されている数種類のオペレーターをオーバーロードして実装することができる。  
<a href="https://kotlinlang.org/docs/reference/operator-overloading.html" target="_blank">Operator overloading - Kotlin Programming Language</a>
　　
```Kotlin
data class Point(val x: Int, val y: Int)
operator fun Point.plus(that: Point) = Point(this.x + that.x, this.y + that.y)

val p1 = Point(10, 10)
val p2 = Point(15, 20)

p1 + p2 // -> Point(25, 30)

// もちろんこれもOK 
p1.plus(p2) // -> Point(25, 30)
```

Note: 
もちろんplusオペレーターを拡張関数で実装するのではなくて、データクラスの実装で書いても大丈夫。
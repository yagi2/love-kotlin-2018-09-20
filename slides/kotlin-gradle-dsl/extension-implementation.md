## 拡張関数のケース
<br />

```kotlin
dependencies.implementation("androidx.constraintlayout:constraintlayout:1.1.3")
```
<br />

`dependencies`は`DependencyHandler`クラスを返す`getDependencies()`  
その`DependencyHandler`クラスに対して、拡張関数が生えている  
  
```Kotlin
fun DependencyHandler.`implementation`(dependencyNotation: Any): Dependency =
    add("implementation", dependencyNotation)
```  

Note: 
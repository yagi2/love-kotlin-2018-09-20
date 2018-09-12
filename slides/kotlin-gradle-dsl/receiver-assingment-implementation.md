## レシーバ指定のラムダ式をとるケース
<br />

```kotlin
dependencies {
    implementation("androidx.constraintlayout:constraintlayout:1.1.3")
}
```
`dependencies`の実態は  

```Kotlin
class DependencyHandlerScope(val dependencies: DependencyHandler) : DependencyHandler by dependencies {
    fun Project.dependencies(configuration: DependencyHandlerScope.() -> Unit) =
        DependencyHandlerScope(dependencies).configuration()
}
```  

`DependencyHandlerScope`クラスを指定したラムダ式を取っているため

```Kotlin
dependencies {
    // ここのthisはDependencyHandlerScope
}
```
`DependencyHandlerScope`は`DependencyHandler`を継承しているので、その中で呼んでる`implementation`はさっきの拡張関数。

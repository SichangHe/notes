# Kotlin

## pattern matching

```kotlin
when (var0) {
    LITERAL -> // …
    in 0..5 -> // …
    is TYPE -> // …
    else -> // …
}
```

## nullability

declare nullable variable

```kotlin
var0: TYPE?
```

### access field in nullable variable

return `null` if `var0` is `null` using safe-call operator

```kotlin
var0?.field
```

assume not-null using non-null assertion operator

```kotlin
var0!!.field
```

return `default_var0` if `null` using Elvis operator

```kotlin
var0?.field ?: default_var0
```

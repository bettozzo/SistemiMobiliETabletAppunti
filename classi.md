# Classi

### Sintassi

```kotlin
class className{
    val field1: Type,
    val field2: Type,
    ...
}
```

### Generics

```kotlin
class className<GenericType>{
    val field1: GenericType,
    val field2: SpecificType,
    ...
}
```

### Instansazione

```kotlin
val instance = className<Generic>(parameters)
```

# Data classes

Classi con solo dati. No metodi.

Automaticamente implementa:

- `equals()`
- `hashCode()`
- `toString()`
- `componentN()`: `component1()`, `component2()`, ...
- `copy()`

**NON** può essere `abstract`, `open`, `sealed` o `inner`

### Sintassi

```kotlin
data class className{
    val field1: Type,
    val field2: Type,
    ...
}
```

# Objects

classe che ha **UNA** sola istanza.

### Sintassi

```kotlin
object objectName{
    val field1: Type,
    val field2: Type,
    ...
}
```

### Instansazione

bisogna darli i valori quando lo istanzi

```kotlin
object ObjectName {
    var field1: Int = 10
    var field2: Int = 3
    ...
}
```

### Chiamare metodo senza instanziare

Si usa `apply()`

```kotlin
val name = ObjectName().apply{
    function1()
    ...
}
```

### Accesso

si fa riferimento ai campi con `.`

```kotlin
ObjectName.propertyName
```

### Companion Object

per oggetti definiti dentro una classe, bisogna aggiungere la parola chiave `companion`

```kotlin
class ClassName{
    val field1:Type,
    val field2:Type,

    companion object ObjectName {
        var field1: Int = 10
        var field2: Int = 3
        ...
    }
}
```

# Estensioni

## Estensioni di Proprietà

### Sintassi

```kotlin
val typeName.propertyName: dataType
    get() = {} //propertyGetter
```

Example:

```kotlin
val Quiz.StudentProgress.progressText: String
    get() = "${answered} of ${total} answered"
```

## Estensioni di funzioni

### Sintassi

```kotlin
fun typeName.functionName(...) : returnType {
    ...
}
```

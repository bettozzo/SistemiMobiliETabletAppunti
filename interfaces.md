# Interfacce

obbligare classe ad implementare metodi definiti dentro l'interface

### Sintassi

```kotlin
interface InterfaceName{
    val field1: Type
    fun functionName()
}
```

### Uso

```kotlin
class ClassName : InterfaceName{
    override val field1: Type
    override fun functionName(){
        ...
    }
}
```

### Accesso

si fa riferimento ai campi con `.`

```kotlin
EnumName.Case1
```

//[qa_sdk](../../../index.md)/[com.quantactions.sdk](../index.md)/[SingletonHolder](index.md)

# SingletonHolder

[androidJvm]\
open class [SingletonHolder](index.md)<out [T](index.md), in [A](index.md)>(**creator**: ([A](index.md)) -> [T](index.md))

## Functions

| Name | Summary |
|---|---|
| [getInstance](get-instance.md) | [androidJvm]<br>fun [getInstance](get-instance.md)(arg: [A](index.md)): [T](index.md) |

## Properties

| Name | Summary |
|---|---|
| [creator](creator.md) | [androidJvm]<br>var [creator](creator.md): ([A](index.md)) -> [T](index.md)? |
| [instance](instance.md) | [androidJvm]<br>@[Volatile](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.jvm/-volatile/index.html)()<br>var [instance](instance.md): [T](index.md)? = null |

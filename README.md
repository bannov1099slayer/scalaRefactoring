# scalaRefactoring

Задача: переписать код ниже в функциональном стиле

```scala
object StringProcessor {
  def processStrings(strings: List[String]): List[String] = {
    var result = List[String]()
    for (str <- strings) {
      if (str.length > 3) {
        result = result :+ str.toUpperCase
      }
    }
    result
  }

  def main(args: Array[String]): Unit = {
    val strings = List("apple", "cat", "banana", "dog", "elephant")
    val processedStrings = processStrings(strings)
    println(s"Processed strings: $processedStrings")
  }
}
```

Переписанный код находится в файле main.scala.
Были внесены изменения:
+ Избавились от изменяемой переменной result и действий над ней;
+ Задействованы функции высшего порядка (filter и map).

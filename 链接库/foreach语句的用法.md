在 C# 中，`foreach` 循环提供了一种简单而直观的方式来遍历集合中的元素，例如数组、列表、字典等。`foreach` 循环的语法结构如下：

``` c#
foreach (var item in collection)
{
    // 循环体，处理每个元素
}
```

其中：

- `var`：用于声明一个局部变量，用于在每次迭代中存储集合中的当前元素。`var` 关键字会根据右侧集合中元素的类型自动推断变量的类型。
- `item`：循环体中使用的变量名，表示集合中的当前元素。
- `collection`：要遍历的集合，可以是数组、列表、字典等支持 `IEnumerable` 或 `IEnumerable<T>` 接口的类型。

下面是一些 `foreach` 循环的常见用法：

1. **遍历数组**：

``` C#
int[] numbers = { 1, 2, 3, 4, 5 };

foreach (var number in numbers)
{
    Console.WriteLine(number);
}
```

2. **遍历列表**：

``` C#
List<string> names = new List<string> { "Alice", "Bob", "Charlie" };

foreach (var name in names)
{
    Console.WriteLine(name);
}
```

3. **遍历字典**：

``` C#
Dictionary<int, string> keyValuePairs = new Dictionary<int, string>
{
    { 1, "One" },
    { 2, "Two" },
    { 3, "Three" }
};

foreach (var pair in keyValuePairs)
{
    Console.WriteLine($"Key: {pair.Key}, Value: {pair.Value}");
}
```

4. **遍历字符串**：

``` C#
string text = "Hello, World!";

foreach (char c in text)
{
    Console.WriteLine(c);
}
```

`foreach` 循环在编译时会被转换为适当的 `for` 循环，以实现对集合的迭代。它是一种简洁和安全的方式来处理集合中的元素，无需担心索引越界或访问不存在的元素。
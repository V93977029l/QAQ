用range-based for 将字符串中的数字逐个导入数组C++

在C++中，你可以使用`range-based for`循环来遍历字符串中的每个字符，并检查它们是否为数字。如果是数字，你可以使用`std::string`的`push_back`方法将其转换为相应的整数值，并添加到数组（或更准确地说，`std::vector`，因为C++的原生数组不支持动态添加元素）中。

以下是一个简单的示例，说明如何实现这个过程：

``` cpp
#include <iostream>
#include <vector>
#include <string>

int main() {
    std::string str = "a1b2c3d4";  // 示例字符串
    std::vector<int> numbers;  // 创建一个整数向量来存储数字

    for (char c : str) {  // 遍历字符串中的每个字符
        if (isdigit(c)) {  // 检查当前字符是否为数字
            numbers.push_back(c - '0');  // 将字符转换为整数并添加到向量中
        }
    }

    // 输出结果
    std::cout << "Extracted numbers: ";
    for (int num : numbers) {
        std::cout << num << " ";
    }
    std::cout << std::endl;

    return 0;
}
```

这段代码首先定义了一个示例字符串`str`和一个整数向量`numbers`。然后，它使用`range-based for`循环遍历字符串中的每个字符。如果字符是数字（使用`isdigit`函数检查），该字符将被转换为相应的整数（通过从字符中减去`'0'`）并添加到`numbers`向量中。

最后，代码遍历`numbers`向量并打印出存储的数字。

请注意，这里使用的是`std::vector<int>`来代替传统的数组，因为向量允许你动态地添加元素，而传统的C++数组则不允许这样做。
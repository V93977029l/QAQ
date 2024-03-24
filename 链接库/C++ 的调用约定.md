C/C++ 的调用约定通常可以在编译器的文档中找到。每个编译器都可能有自己的调用约定，并且可能提供不同的选项。以下是一些常见的 C/C++ 编译器和它们的调用约定：

1. **Microsoft Visual C++ (MSVC)**:
    
    - 默认调用约定是 `__cdecl`。
    - 托管 C++ 使用 `__clrcall`。
    - 可以通过 `__stdcall` 指定标准调用约定。
    
    MSVC 文档链接：[MSVC Calling Conventions](https://docs.microsoft.com/en-us/cpp/cpp/calling-conventions?view=msvc-160)
    
2. **GNU Compiler Collection (GCC)**:
    
    - 默认调用约定是 `__cdecl`。
    - 可以通过 `__stdcall` 或 `__fastcall` 指定其他调用约定。
    
    GCC 文档链接：[i386 and x86-64 Options](https://gcc.gnu.org/onlinedocs/gcc/x86-Options.html)
    
3. **Clang**:
    
    - 默认调用约定是 `__cdecl`。
    - 支持 `__stdcall`、`__fastcall` 等调用约定。
    
    Clang 文档链接：[Calling Conventions](https://clang.llvm.org/docs/LanguageExtensions.html#calling-conventions)
    

在查看特定编译器的调用约定时，最好查阅相应的官方文档。此外，特定平台和体系结构也可能对调用约定产生影响，因此了解目标平台的规定也是重要的。
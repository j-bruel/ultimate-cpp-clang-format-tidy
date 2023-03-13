# ultimate-cpp-clang-format-tidy

The ultimate C++ clang format & tidy.

## Tools you need to have

### Clang-format

Clang-Format is a tool that automatically formats C++ code based on a set of rules and options.
It can help ensure consistency in code formatting across a project and improve code readability.
Clang-Format is part of the Clang compiler suite and is based on the LLVM project.
It can be used from the command line or integrated into an IDE such as Visual Studio Code or Xcode.

### Clang-tidy

Clang-Tidy is a tool that analyzes C++ code and provides suggestions for improvements based on a set of rules and checks.
It can help identify potential bugs, security issues, and code smells in a codebase.
Clang-Tidy is also part of the Clang compiler suite and is based on the LLVM project.
Like Clang-Format, it can be used from the command line or integrated into an IDE.

### Why you should have it into your project

Overall, Clang-Format and Clang-Tidy can help improve code quality, consistency, and maintainability.
They can be especially useful in large codebases where manual formatting and checking would be time-consuming and error-prone.

## Trigger warning

Both Clang-Format and Clang-Tidy are highly configurable and customizable.
They offer a wide range of options and settings that can be tailored to a project's specific needs and coding style.

**Conclusion**: Current clang-format & clang-tidy files corresponding to my personal vision. You are welcome to duplicate theses files and update it as you wish.

## Visual Studio integration

They can also be integrated into a project's build system to automatically format and check code as part of the build process.

1. Copy the .clang-tidy and the .clang-format file into the main directory of your c++ project.

Great, your clang-format is ready ! Open any C++ file and press Ctrl+K+D and you fille will be automatically formatted.

2. Set the CMAKE_CXX_CLANG_TIDY variable into your CMakeLists.txt file to enable your clang-tidy at build time.

I recommend you to precede this way:

Into your CMakeLists.txt:

```cmake
if (ENABLE_CLANG_TIDY)
	set(CMAKE_CXX_CLANG_TIDY clang-tidy)
endif()
```

Into your main / common CMakePresets configuration:

```json
"cacheVariables": {
	"ENABLE_CLANG_TIDY": false
}
```

Into your CMakePresets template and CMakeUserPresets.json

```json
"cacheVariables": {
	"ENABLE_CLANG_TIDY": true
}
```
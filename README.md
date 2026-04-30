# StarByte Language Support for VS Code

Syntax highlighting and editor support for the
[StarByte](https://github.com/StarByteGames/StarByte) programming language
(`.sb` files).

StarByte is a fast, modern, general-purpose language with C-level
performance and C#-style ergonomics. This extension gives you a
first-class editing experience for it.

## Features

- **Full syntax highlighting** for StarByte sources (`.sb`)
    - Control-flow keywords: `if`, `else`, `for`, `while`, `do`,
      `switch`, `case`, `default`, `break`, `continue`, `return`
    - Declarations: `module`, `struct`, `enum`, `class`, `interface`,
      `func`, `const`, `static`, `public`, `private`, `protected`,
      `extends`, `implements`, `new`, `this`, `super`
    - Memory & exceptions: `alloc`, `free`, `gc_alloc`, `gc_collect`,
      `len`, `try`, `catch`, `finally`, `throw`
    - Built-in types: `int`, `float`, `double`, `char`, `string`,
      `bool`, `void`, `byte`, `short`, `long`, `uint`, `ulong`,
      `ushort`, `sbyte`
    - Constants: `true`, `false`, `null`
    - Preprocessor directives: `#if`, `#elif`, `#else`, `#endif`,
      `#define`, `#include`
- **String / char literals** with escape sequences (`\n`, `\t`, `\r`,
  `\\`, `\"`, `\'`, `\0`, hex/unicode escapes).
- **Numeric literals**: integers, floats (with exponent), hex (`0x...`)
  and binary (`0b...`).
- **Operator highlighting** for arithmetic, comparison, logical,
  bitwise, assignment / compound-assignment, increment/decrement, and
  the ternary operator.
- **Function definition vs. function call** highlighted distinctly.
- **PascalCase identifiers** highlighted as type/class names.
- **Comments**: line `//` and block `/* ... */`.
- **Editor configuration**: bracket matching, auto-closing pairs,
  surrounding pairs, smart indentation, and `// #region` /
  `// #endregion` folding markers.

## Installation

### From a packaged VSIX

```sh
code --install-extension starbyte-language-<version>.vsix
```

### From source (development)

1. Clone this repository.
2. Open the folder in VS Code.
3. Press `F5` to launch an Extension Development Host with the
   extension loaded.
4. Open any `.sb` file (e.g. [examples/test.sb](examples/test.sb)) to
   see the highlighter in action.

### Packaging

Requires [`@vscode/vsce`](https://github.com/microsoft/vscode-vsce):

```sh
npm install -g @vscode/vsce
vsce package
```

This produces a `starbyte-language-<version>.vsix` file you can
distribute or install locally.

## Usage

Once installed, any file with the `.sb` extension is automatically
recognized as StarByte. You can also force the language mode from the
status bar (bottom-right) by clicking the language indicator and
choosing **StarByte**.

A demonstration source file lives at
[examples/test.sb](examples/test.sb) — open it to verify that all
token classes are highlighted as expected.

## About StarByte

StarByte ships with a tree-walking interpreter, a native compiler
backend (transpiles to C and invokes the system C compiler), and a
small standard library (`Console`, `Math`, `Strings`, `Memory`).

```cs
module System.Console;

int main() {
    Console.WriteLine("Hello, StarByte!");
    return 0;
}
```

See the official [language reference](https://github.com/StarByteGames/StarByte/blob/main/docs/LANGUAGE.md)
for the complete syntax.

## Release Notes

See [CHANGELOG.md](CHANGELOG.md).

## License

MIT.

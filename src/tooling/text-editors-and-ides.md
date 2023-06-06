# Visual Studio Code

A widely used development environment for Rust programming is Microsoft's [Visual Studio Code] text editor, often accompanied by the [Rust Analyzer] extension.

Visual Studio Code is a versatile, open-source, and cross-platform graphical text editor that offers an extensive range of extensions. The [Rust Analyzer extension], specifically designed for Rust development, implements the [Language Server Protocol]. It enhances the editing experience by providing features such as autocompletion, navigation to definitions, and more.

To install Visual Studio Code, you can utilize popular package managers or download the installers directly from the [official website][vscode-installer]. Within Visual Studio Code, you can easily install the  [Rust Analyzer extension] through the built-in extension manager.

Alongside Rust Analyzer (RA),there are other valuable extensions that can enhance your Rust development experience:

- [Better TOML] for editing TOML-based configuration files
- [crates] to help manage Rust dependencies

[visual studio code]: https://code.visualstudio.com/
[rust analyzer]: https://rust-analyzer.github.io/
[Rust Analyzer extension]: https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer
[language server protocol]: https://microsoft.github.io/language-server-protocol/
[Better TOML]: https://marketplace.visualstudio.com/items?itemName=bungcip.better-toml
[crates]: https://marketplace.visualstudio.com/items?itemName=serayuzgur.crates
[vscode-installer]: https://code.visualstudio.com/download

## Tips and Tricks

If you are developing for a target that does not have `std` support, Rust Analyzer can behave strangely, often reporting various errors. This can be resolved by creating a `.vscode/settings.json` file in your project and populating it with the following:

```json
{
  "rust-analyzer.checkOnSave.allTargets": false
}
```

If you are using a custom toolchain, as you would with Xtensa targets, you can provide some hints to `cargo` via the `rust-toolchain.toml` file to improve the user experience:

```toml
[toolchain]
channel = "esp"
components = ["rustfmt", "rustc-dev"]
targets = ["xtensa-esp32-none-elf"]
```

## Other IDEs

There are other IDEs like [CLion] or [vim] that also have pretty good support for Rust,
but we won't be covering them here.

[CLion]: https://www.jetbrains.com/clion/
[vim]: https://www.vim.org/

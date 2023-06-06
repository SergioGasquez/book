# Wokwi

[Wokwi] is an online simulator that provides support for simulating Rust projects on ESP Chips, including both `std` and `no_std` development. You can visit [wokwi.com/rust] to access a variety of examples and initiate new projects.

Wokwi offers a range of features, including Wi-Fi simulation, Virtual Logic Analyzer, and [GDB debugging], among otherss, see [Wokwi documentation] for more details. For ESP chips, there is a [table available that outlines the currently supported simulation features].

## Using Wokwi for VS Code extension
Wokwi provides a convenient VS Code extension that enables users to simulate their projects directly from their code editor by simply adding a few files. To learn more about this feature, you can refer to the [Wokwi documentation][wokwi-vscode]. Additionally, you can utilize the VS Code debugger to debug your code effectively. For detailed instructions on how to use the debugger, please consult the documentation on [debugging with Wokwi].

When using any of the [templates] and not using the default values, there is a prompt (`Configure project to support Wokwi simulation with Wokwi VS Code extension?`) that generates the required files to use Wokwi VS Code extension.

![Wokwi VS Code example](../../assets/wokwi-vscode.png)

## Using wokwi-server

[wokwi-server] also allows simulating your resulting binary on other Wokwi projects, with more hardware parts other than the chip itself. See the [corresponding section of the wokwi-server README] for detailed instructions.
Moreover, [wokwi-server] provides the capability to simulate your generated binary alongside additional hardware components in other Wokwi projects. For comprehensive instructions on how to utilize this functionality, please refer to the [corresponding section of the wokwi-server README], where you will find detailed guidance.

## Custom chips
Wokwi provides the capability to generate custom chips, allowing you to define the behavior of components that are not natively supported in Wokwi. For detailed information on how to create and utilize custom chips, please refer to the official  [Wokwi documentation][wokwi-custom-chip].

Notably, you can also develop custom chips using Rust programming language. The [Wokwi Custom Chip API][rust-chip-api] documentation offers comprehensive details on how to leverage Rust to create custom chips. As an example, you can explore the implementation of a custom [inverter chip][custom-chip-example] written in Rust, which demonstrates the possibilities of utilizing Rust for custom chip development.

[Wokwi]: https://wokwi.com/
[wokwi.com/rust]: https://wokwi.com/rust
[GDB debugging]: https://docs.wokwi.com/gdb-debugging
[Wokwi documentation]: https://docs.wokwi.com/
[table available that outlines the currently supported simulation features]: https://docs.wokwi.com/guides/esp32#simulation-features
[wokwi-server]: https://github.com/MabezDev/wokwi-server
[corresponding section of the wokwi-server Readme]: https://github.com/MabezDev/wokwi-server#simulating-your-binary-on-a-custom-wokwi-project
[wokwi-vscode]: https://docs.wokwi.com/vscode/getting-started
[debugging with Wokwi]: https://docs.wokwi.com/vscode/debugging
[templates]: ./../../writing-your-own-application/generate-project/index.md
[wokwi-custom-chip]: https://docs.wokwi.com/chips-api/getting-started
[custom-chip-example]: https://github.com/wokwi/rust_chip_inverter
[rust-chip-api]: https://github.com/wokwi/wokwi_chip_ll

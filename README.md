# Gradle Remote Versioned Modular Script Plugin

This source code is part of [Gradle build tool example projects](https://github.com/rivancic/gradle).

It contains Gradle script plugin that will be used in the lecture explaining remote versioned modular script plugin. It holds specific build logic in a separate files.

Part of the naming is already explained at [remote versioned script plugin repository page](https://github.com/rivancic/gradle-versioned-script-plugin).

Modular is an additional functionality for this example.

- **Modular**: For maintainability and structure of ever evolving software we need to keep it modular. This can be done on different levels. For script plugins a natural way is to split them in separate files that can be referenced in other scripts. Similar like classes can be imported into others. With the modular script plugins we can build different script plugins reusing functionality.

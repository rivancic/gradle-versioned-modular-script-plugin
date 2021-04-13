# Gradle Versioned Modular Remote Script Plugin Example

This source code is part of [Gradle build tool example projects](https://github.com/rivancic/gradle).

It contains Gradle script plugin that will be used in the lecture explaining remote versioned modular script plugin. It holds specific build logic in a separate files.

Part of the naming is already explained at [remote versioned script plugin repository page](https://github.com/rivancic/gradle-versioned-script-plugin).

Modular is an additional functionality for this example.

- **Modular**: For maintainability and structure of ever evolving software we need to keep it modular. This can be done on different levels. For script plugins a natural way is to split them in separate files that can be referenced in other scripts. Similar like classes can be imported into others. With the modular script plugins we can build different script plugins reusing functionality.

## Usage

You can import two different flavors of modularized plugins:

1) To configure build functionality for Java libraries:

`apply from: 'https://raw.githubusercontent.com/rivancic/gradle-versioned-modular-script-plugin/v1.0/java-library-plugin.gradle'`

It will include:
- Java
- Junit Test

2) Configuring build pipeline for Spring Boot application:

`apply from: 'https://raw.githubusercontent.com/rivancic/gradle-versioned-modular-script-plugin/v1.0/spring-application-plugin.gradle'`

It will include:
- Java
- Spring Boot
- Junit
- Cucumber + Selenium E2E

Note: A specific version of the plugin can be provided, check release notes for changes or additional functinality in 
different versions.


## Explanation

In concrete example the emphasis is put on the plugin modularity.
This is logical next step after extracting build logic from the main build.gradle file.
Its guaranteed that the build logic in bigger project will expand with specific requirements we have to be able
to separate different concerns of building process into separate files.

For example, for very simple project maybe is enough to only compile and package the code into a jar file.
Compilation of the source code is dependent on the language its written in.
Packaging of the application highly depends on the type of the framework the application was written in.

Often times one of the basic requirements is that the source code is tested with tests that can be applied on different layers.

This means additionally to compilation of source code and packaging the application we also have to support different kinds of 
source code or application testing.

Unit testing (Junit, TestNG, ..)
Integration testing (Wiremock, In memory databases, SpringBoot testing, Testcontainers)
E2E tests (Selenium, ...)

Building process can be expanded with plethora of other intermediary steps that help software engineers...



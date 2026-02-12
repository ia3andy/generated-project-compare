# Code With Quarkus Projects Comparison

This repository helps you compare Quarkus project generator (code.quarkus.io) across different versions and build tools.

## 🏗️ Repository Structure

This repository uses a **multi-branch architecture** where each build tool has its own dedicated branch:

- **[workflow](https://github.com/quarkusio/code-with-quarkus-compare/tree/workflow)** - Contains the GitHub Actions workflow (this branch)
- **[maven](https://github.com/quarkusio/code-with-quarkus-compare/tree/maven)** - Maven projects in root directory
- **[gradle](https://github.com/quarkusio/code-with-quarkus-compare/tree/gradle)** - Gradle projects in root directory
- **[gradle-kotlin-dsl](https://github.com/quarkusio/code-with-quarkus-compare/tree/gradle-kotlin-dsl)** - Gradle Kotlin DSL projects in root directory

Each branch contains the generated project files directly in the root directory (no subdirectories).

## 🏷️ Tagging System

Projects are tagged using the format: `buildtool-version`

Examples:
- `maven-3.15.7`
- `maven-3.31.2`
- `gradle-3.31.2`
- `gradle-kotlin-dsl-3.31.2`

## 🔍 Comparing Versions

You can compare any two versions using GitHub's compare view:

### Maven Projects
Compare Maven project changes between Quarkus 3.15.7 and 3.31.2:
```
https://github.com/quarkusio/code-with-quarkus-compare/compare/maven-3.15.7...maven-3.31.2
```

### Gradle Projects
Compare Gradle project changes between versions:
```
https://github.com/quarkusio/code-with-quarkus-compare/compare/gradle-3.15.7...gradle-3.31.2
```

### Gradle Kotlin DSL Projects
Compare Gradle Kotlin DSL project changes:
```
https://github.com/quarkusio/code-with-quarkus-compare/compare/gradle-kotlin-dsl-3.15.7...gradle-kotlin-dsl-3.31.2
```

### Compare Across Build Tools
You can also compare the same version across different build tools:
```
https://github.com/quarkusio/code-with-quarkus-compare/compare/maven-3.31.2...gradle-3.31.2
```

## 📋 Available Tags

View all available tags: [Tags](https://github.com/quarkusio/code-with-quarkus-compare/tags)

## 🛠️ How It Works

1. The **workflow** branch contains a GitHub Actions workflow
2. When triggered, it runs in parallel for all build tools (Maven, Gradle, Gradle Kotlin DSL)
3. For each build tool:
   - Generates a new Quarkus project using the given Quarkus version (and a Quarkus CLI in the same version)
   - Checks out the corresponding branch
   - Replaces all content with the newly generated project
   - Commits and pushes the changes
   - Tags the commit with `buildtool-version`

> [!IMPORTANT]
> When generating older Quarkus projects using the latest Quarkus CLI (or code.quarkus.io), the result may differ because some base templates are embedded in the CLI. For clarity and consistency, we chose to keep those templates aligned during generation so that differences are clearly visible.

## 📖 Example Workflows

### See what changed in Maven projects from 3.15 to 3.31
[Compare maven-3.15.7...maven-3.31.2](https://github.com/quarkusio/code-with-quarkus-compare/compare/maven-3.15.7...maven-3.31.2)

### See differences between Maven and Gradle for version 3.31.2
[Compare maven-3.31.2...gradle-3.31.2](https://github.com/quarkusio/code-with-quarkus-compare/compare/maven-3.31.2...gradle-3.31.2)

---

Generated with ❤️ for the Quarkus community

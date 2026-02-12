# Quarkus Generated Project Comparison

This repository helps you compare Quarkus project scaffolding across different versions and build tools.

## 🏗️ Repository Structure

This repository uses a **multi-branch architecture** where each build tool has its own dedicated branch:

- **[workflow](https://github.com/ia3andy/generated-project-compare/tree/workflow)** - Contains the GitHub Actions workflow (this branch)
- **[maven](https://github.com/ia3andy/generated-project-compare/tree/maven)** - Maven projects in root directory
- **[gradle](https://github.com/ia3andy/generated-project-compare/tree/gradle)** - Gradle projects in root directory
- **[gradle-kotlin-dsl](https://github.com/ia3andy/generated-project-compare/tree/gradle-kotlin-dsl)** - Gradle Kotlin DSL projects in root directory

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
https://github.com/ia3andy/generated-project-compare/compare/maven-3.15.7...maven-3.31.2
```

### Gradle Projects
Compare Gradle project changes between versions:
```
https://github.com/ia3andy/generated-project-compare/compare/gradle-3.15.7...gradle-3.31.2
```

### Gradle Kotlin DSL Projects
Compare Gradle Kotlin DSL project changes:
```
https://github.com/ia3andy/generated-project-compare/compare/gradle-kotlin-dsl-3.15.7...gradle-kotlin-dsl-3.31.2
```

### Compare Across Build Tools
You can also compare the same version across different build tools:
```
https://github.com/ia3andy/generated-project-compare/compare/maven-3.31.2...gradle-3.31.2
```

## 🚀 Generating New Projects

To generate new project snapshots:

1. Go to [Actions](https://github.com/ia3andy/generated-project-compare/actions/workflows/generate-quarkus-projects.yml)
2. Click **"Run workflow"**
3. Optionally specify a Quarkus version (leave empty for latest)
4. The workflow will generate projects for all three build tools in parallel

The workflow will:
- Generate fresh projects using the Quarkus CLI
- Commit them to their respective branches
- Tag each commit with `buildtool/version` format

## 📋 Available Tags

View all available tags: [Tags](https://github.com/ia3andy/generated-project-compare/tags)

## 💡 Use Cases

- **Track Quarkus Changes**: See what changes between Quarkus versions in generated projects
- **Migration Planning**: Understand what needs updating when upgrading Quarkus
- **Build Tool Comparison**: Compare how different build tools structure the same project
- **Regression Detection**: Spot unexpected changes in project generation

## 🛠️ How It Works

1. The **workflow** branch contains a GitHub Actions workflow
2. When triggered, it runs in parallel for all build tools (Maven, Gradle, Gradle Kotlin DSL)
3. For each build tool:
   - Generates a new Quarkus project using the CLI
   - Checks out the corresponding branch
   - Replaces all content with the newly generated project
   - Commits and pushes the changes
   - Tags the commit with `buildtool-version`

## 📖 Example Workflows

### See what changed in Maven projects from 3.15 to 3.31
[Compare maven-3.15.7...maven-3.31.2](https://github.com/ia3andy/generated-project-compare/compare/maven-3.15.7...maven-3.31.2)

### See differences between Maven and Gradle for version 3.31.2
[Compare maven-3.31.2...gradle-3.31.2](https://github.com/ia3andy/generated-project-compare/compare/maven-3.31.2...gradle-3.31.2)

---

Generated with ❤️ for the Quarkus community
# Copilot Instructions for UnitConverterApp

## Project Overview
- **UnitConverterApp** is a modern Android app for converting length units (meters, centimeters, feet, millimeters) with a focus on clean UI and real-time results.
- Built using **Kotlin**, **Jetpack Compose**, and **Material3** for a declarative, modern Android experience.

## Architecture & Key Patterns
- The app uses a **single-module, Compose-first architecture**: UI, state, and logic are colocated in composable functions.
- **No legacy XML layouts**: All UI is defined in Kotlin using Compose.
- **Conversion logic** is likely implemented in a dedicated Kotlin file/class, separated from UI code for testability and clarity.
- **Material3 theming** is used throughout for consistent look and feel.

## Developer Workflows
- **Build & Run:**
  - Use Android Studio or run `./gradlew assembleDebug` to build.
  - Launch on emulator/device via Android Studio or `./gradlew installDebug`.
- **Testing:**
  - (If present) Run unit tests with `./gradlew test`.
- **Dependencies:**
  - Managed via Gradle Kotlin DSL (`build.gradle.kts`).
  - Jetpack Compose and Material3 are core dependencies.

## Project Conventions
- **UI logic** is colocated with composables; avoid fragment/activity-based patterns.
- **Precision:** All conversions display up to 4 decimal places.
- **Dropdowns** are used for unit selection; input is validated for numeric values.
- **Naming:** Use clear, descriptive names for composables and conversion functions (e.g., `convertLength`, `UnitDropdown`).
- **No dark mode** or history features yet—future improvements are listed in `README.md`.

## Key Files & Directories
- `build.gradle.kts` – Gradle build config, dependencies
- `README.md` – Project overview, features, and roadmap
- Main source files (likely in `app/src/main/java/` or similar) – UI and logic

## Integration Points
- No external APIs or network dependencies; all logic is local.
- Material3 and Jetpack Compose are the primary external libraries.

## Example Patterns
- Use composable functions for all UI elements:
  ```kotlin
  @Composable
  fun UnitConverterScreen() { /* ... */ }
  ```
- Separate conversion logic from UI for testability:
  ```kotlin
  fun convertLength(value: Double, from: Unit, to: Unit): Double { /* ... */ }
  ```

## When in Doubt
- Follow Jetpack Compose and Material3 best practices.
- Keep UI and logic modular and testable.
- Reference `README.md` for feature scope and future plans.

# C# Professional Standards & Clean Code Guidelines

You are an expert C# mentor. Ensure all code generated or refactored for junior engineers adheres to these standards to maintain high quality before PRs are raised.

## 1. SOLID Principles
- **Single Responsibility**: Each class and method must have one, and only one, reason to change.
- **Open/Closed**: Classes should be open for extension but closed for modification.
- **Liskov Substitution**: Derived classes must be substitutable for their base classes.
- **Interface Segregation**: Prefer many small, client-specific interfaces over one large general-purpose one.
- **Dependency Inversion**: Depend on abstractions (interfaces), not concrete implementations. Use Constructor Injection.

## 2. Code Organization & Order
- **Vertical Proximity**: Keep related functions close to each other. If Method A calls Method B, they should be vertically adjacent.
- **The Step-Down Rule**: Arrange code like a newspaper—high-level logic at the top, low-level details at the bottom.
- **Standard Member Order**:
    1. Private fields (prefixed with `_`)
    2. Constructors
    3. Public Properties
    4. Public Methods
    5. Private/Protected helper methods (placed immediately below the public method that uses them)

## 3. Auto Testing (AAA Pattern)
- **Structure**: All unit tests must follow the **Arrange, Act, Assert** pattern with clear comments separating each phase.
- **Naming**: Follow the `StateUnderTest_MethodName_ExpectedBehavior` convention.
- **Isolation**: Use Mocks/Interfaces to ensure tests do not touch the database or file system.
- **F.I.R.S.T**: Tests must be Fast, Independent, Repeatable, Self-validating, and Timely.

## 4. Code Documentation
- **README**: Document application setup and core features in the `README.md`.
- **Implementation Details**: Use comments to explain *why* (rationale), not *what* (logic).
- **Meaningful Docstrings**: Write XML documentation (`///`) for all public modules, classes, and functions.
- **Code over Comments**: Prioritize clean code over excessive commenting. Refactor before explaining.
- **Clean Docs**: Remove unused parameters from docstrings immediately.

## 5. Branching & Workflow
- **Branch Naming**: Strictly follow the format: `feat/user_name/short-description` (e.g., `feat/jdoe/add-login-logic`).
- **Atomic Commits**: Ensure each commit handles one logical change to make PR reviews easier.

## 6. Function Design & Immutability
- **Small Scope**: Methods should ideally be under 20 lines.
- **Parameter Count**: Aim for 0–2 arguments. Use a class/struct for 3+ parameters.
- **CQS**: A method should either change state or return data, never both.
- **Read-Only**: Use the `readonly` keyword for fields that do not change after the constructor.

## 7. Naming & Formatting
- **Naming**: `PascalCase` for public members; `camelCase` for locals/parameters; `_camelCase` for private fields.
- **4-Space Indentation**: Use exactly 4 spaces (no tabs).
- **Braces**: Use Allman style (braces on new lines). Always use braces even for single-line statements.

## 8. Exception Handling & Resources
- **Preserve Stack**: Use `throw;` to re-throw, never `throw ex;`.
- **No Swallowing**: Never use empty catch blocks. Always log the error.
- **Deterministic Disposal**: Use `using` blocks for all `IDisposable` types (Streams, DB connections).
- **No Magic Values**: Replace hardcoded strings/numbers with `const` or `enums`.

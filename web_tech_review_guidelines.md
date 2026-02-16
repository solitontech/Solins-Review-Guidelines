# Web Technology Review Guidelines

## 1. Naming Conventions

- Avoid single-character names like `i`, `j`, `c`
- Use meaningful, short names
- Use `camelCase` for variables and functions
- Use `PascalCase` for classes and components
- Use `kebab-case` for file and folder names
- Use `UPPER_CASE` for constants
- Maintain consistent naming across the project

## 2. Modularity & Readability

- Code should be readable, modular, and scalable
- Follow SOLID principles where applicable
- Keep functions short and focused
- One responsibility per function
- Use meaningful identifiers
- Group related functions and logic by feature or domain
- Separate responsibilities into dedicated modules (API, UI, Utils,
  State, etc.)
- Avoid deeply nested conditionals, loops, and callbacks
- Prefer early returns and smaller functions to reduce nesting levels
- Avoid overly complex CSS selector chains
- Use blank lines to separate logical blocks
- Avoid overly complex or clever code
- Remove unused code

## 3. Project Structure

- Maintain a clear folder hierarchy
- Separate assets, styles, scripts, and modules
- Avoid mixing business logic with UI logic
- Keep reusable components in separate folders
- Avoid deeply nested directories

## 4. HTML Best Practices

- Use semantic HTML5 tags
- Maintain proper heading hierarchy
- Always add `alt` attributes to images
- Use `title` attributes where needed
- Follow valid HTML nesting rules
- Use meta viewport for responsiveness
- Avoid excessive `<div>` and `<span>` usage
- Ensure accessibility compliance

## 5. CSS Best Practices

- Use CSS variables for colors, fonts, and spacing
- Group color variables in a separate file
- Apply reset or normalize styles
- Prefer Flexbox and Grid for layouts
- Avoid excessive nesting
- Use `box-sizing: border-box`
- Avoid `!important` unless necessary
- Follow consistent naming conventions
- Use shorthand properties
- Organize properties logically
- Keep CSS properties in alphabetical order
- Use media queries for responsiveness

## 6. JavaScript Coding Standards

- Prefer `const` and `let` over `var`
- Use destructuring where applicable
- Use template literals for strings
- Avoid magic numbers and strings
- Use arrow functions appropriately
- Keep functions small and reusable
- Avoid global variables
- Use meaningful function and variable names

## 7. Modularity & Reusability

- Use ES module `import` and `export`
- Avoid duplicated logic
- Create reusable utilities and helpers
- Follow separation of concerns
- Group related functionalities

## 8. DOM & Performance

- Minimize direct DOM manipulation
- Avoid repeated or unnecessary use of `innerHTML`
- Clear containers before re-rendering when required
- Use `DocumentFragment` where applicable
- Prefer event delegation
- Avoid inline event handlers
- Prevent unnecessary reflows and repaints
- Batch DOM updates whenever possible

## 9. Dynamic UI & Input Handling

- Validate user input and handle invalid values gracefully
- Provide fallback or NIL values when data is missing
- Support keyboard navigation for inputs and dropdowns
- Update UI elements dynamically based on state changes
- Avoid hardcoding dynamic values
- Use closures or IIFE for scoped logic when needed

## 10. Filtering, Pagination & Scrolling

- Use `filter`, `map`, and `reduce` for data processing
- Validate boundary conditions
- Show meaningful feedback for invalid inputs
- Hide or show UI controls based on content overflow
- Add smooth scrolling and UI animations responsibly
- Avoid duplicating filtering logic

## 11. Sorting & Data Integrity

- Never mutate original data while sorting
- Always work on copied arrays
- Support multi-level sorting when required
- Use clear and readable sort logic
- Minimize DOM updates during re-render
- Batch DOM updates using fragments or buffers

## 12. Error Handling & Validation

- Use `try/catch` for async operations
- Handle API failures gracefully
- Validate user inputs and API responses
- Show meaningful fallback messages
- Avoid silent failures
- Log errors appropriately

## 13. Async, Promises & Timers

- Prefer `async/await` over chained promises
- Do not mix `then()` with `await`
- Use `Promise.all()` for parallel operations
- Always clear intervals and timeouts when unused
- Wrap `await` calls in `try/catch`
- Ensure async functions return Promises
- Use `.finally()` for cleanup
- Avoid unnecessary Promise wrapping

## 14. ES6 Classes & Inheritance

- Always use `extends` and `super()` for inheritance
- Keep base classes generic and reusable
- Avoid deeply nested class hierarchies
- Use camelCase for methods and PascalCase for class names
- Initialize all required properties in constructors
- Keep classes small and single-purpose
- Avoid arrow functions for class methods unless required

## 15. Prototype Best Practices

- Prefer `Object.create()` over `__proto__`
- Never modify global prototypes
- Avoid deep prototype chains
- Do not reassign base prototypes after inheritance
- Define shared methods on prototypes
- Override behavior instead of modifying base prototypes
- Use `this` carefully and consistently

## 16. Advanced JavaScript Patterns

- Use closures for data privacy
- Avoid polluting global scope
- Prefer ES6 classes where suitable
- Avoid deep inheritance chains

## 17. Code Documentation

- Add comments only when necessary
- Prefer self-explanatory code

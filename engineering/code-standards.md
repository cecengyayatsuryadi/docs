# Code Standards

> Coding conventions, patterns, and style rules for this project.

**Last updated:** YYYY-MM-DD

---

## General Standards

### Code Organization

| Principle | Rule |
|-----------|------|
| Single responsibility | One module/class/function = one job |
| Composition over inheritance | Build from small, composable pieces |
| Co-location | Keep related files together (module, tests, types) |
| Explicit over implicit | Prefer clear, verbose code over clever shortcuts |

### Type Safety

- Use your language's type system fully
- Avoid dynamic typing escape hatches (e.g. `any`, `object`, `interface{}`)
- Define data shapes / models explicitly
- Prefer strict compiler/interpreter settings

### Error Handling

- Handle errors explicitly — never silently swallow them
- Use your language's error conventions (exceptions, Result types, error returns)
- Log errors with enough context to debug later
- Provide meaningful error messages

---

## Project Stack

> Fill in with your project's actual technologies.

| Layer | Tech |
|-------|------|
| Language | [e.g. Python 3.12, TypeScript, Go, Rust, Java] |
| Framework | [e.g. Django, FastAPI, Express, Gin, Actix, Spring] |
| Data access | [e.g. SQLAlchemy, Drizzle, GORM, Diesel, JPA] |
| Testing | [e.g. pytest, Vitest, go test, cargo test, JUnit] |
| Linting | [e.g. Ruff, ESLint, golangci-lint, clippy, Checkstyle] |

---

## Code Patterns

> Document correct vs incorrect patterns for your stack.

```
✅ Correct: [describe the right way to do something]

❌ Wrong: [describe the common mistake to avoid]
```

---

## Import / Module Rules

> Document your import conventions.

```
✅ Correct: import from internal module paths
❌ Wrong: import across module boundaries using relative paths
```

---

## UI / Frontend Standards (If Applicable)

> Skip this section if your project has no user interface.

### Accessibility
- All interactive elements must be keyboard-accessible
- Use semantic markup
- Provide accessible labels when visual context is insufficient

### Component Organization
- One component = one job
- Keep related files together (component, styles, tests)

### UI Stack

| Layer | Tech |
|-------|------|
| UI framework | [e.g. React, Vue, Svelte, Angular, HTMX, GTK, Qt] |
| Styling | [e.g. Tailwind, SCSS, CSS Modules, native toolkit] |
| Components | [e.g. shadcn/ui, Vuetify, Material UI, Headless UI] |
| State | [e.g. Zustand, Pinia, Redux, Signals] |
| Forms | [e.g. React Hook Form, VeeValidate, Formik] |
| Validation | [e.g. Zod, Yup, Joi, Pydantic, class-validator] |

---

## When to Update This File

- When coding patterns or conventions change
- When a new library is adopted or removed
- When project stack changes

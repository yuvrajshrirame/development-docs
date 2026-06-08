# Conventional Commits Guide

## Why Use Conventional Commits?

Conventional Commits make your Git history:

* Easier to read
* Easier to search and filter
* More professional
* Better for team collaboration
* Compatible with automated changelog generation
* Helpful for semantic versioning

Instead of writing:

```text
fixed bug
updated code
final changes
```

Write:

```text
fix(auth): resolve token validation issue
feat(ui): add dark mode toggle
docs(readme): update installation instructions
```

---

## Commit Message Structure

```text
<type>(<scope>): <description>
```

### Components

| Component   | Description                 |
| ----------- | --------------------------- |
| type        | Nature of the change        |
| scope       | Area/module affected        |
| description | Short summary of the change |

### Example

```text
feat(auth): add Google OAuth login
```

* `feat` → New feature
* `auth` → Authentication module
* `add Google OAuth login` → Description

---

## Commit Types

### feat

Used when introducing a new feature.

```text
feat(auth): add password reset
feat(chat): implement real-time messaging
feat(ui): add dark mode
```

---

### fix

Used when fixing a bug.

```text
fix(api): handle null responses
fix(auth): resolve login issue
fix(ui): correct mobile layout
```

---

### docs

Used when modifying documentation only.

```text
docs(readme): update setup instructions
docs(api): add endpoint examples
docs(main): improve project overview
```

---

### refactor

Used when restructuring code without changing behavior.

```text
refactor(auth): simplify token handling
refactor(core): remove duplicate logic
refactor(api): reorganize routes
```

---

### style

Used for formatting and styling changes.

```text
style(ui): format components
style(css): reorganize stylesheets
style(main): apply lint fixes
```

---

### test

Used when adding or modifying tests.

```text
test(auth): add login unit tests
test(api): improve endpoint coverage
test(core): add integration tests
```

---

### perf

Used for performance improvements.

```text
perf(api): optimize database queries
perf(cache): reduce lookup time
perf(ui): improve rendering speed
```

---

### chore

Used for maintenance tasks.

```text
chore: initial commit
chore(deps): update dependencies
chore(config): add eslint configuration
```

---

### build

Used for build system changes.

```text
build: configure webpack
build(docker): add Docker support
build(vite): migrate build system
```

---

### ci

Used for CI/CD workflows.

```text
ci(github): add deployment workflow
ci(actions): automate testing
ci(vercel): configure deployment
```

---

### revert

Used when reverting previous commits.

```text
revert(auth): rollback OAuth implementation
revert: remove experimental feature
```

---

## Common Scopes

Scopes help identify which part of the project was modified.

### Frontend

```text
ui
frontend
components
dashboard
profile
```

### Backend

```text
api
backend
server
database
auth
```

### DevOps

```text
docker
github
ci
deployment
```

### Documentation

```text
readme
docs
wiki
```

Examples:

```text
feat(frontend): add landing page
fix(auth): resolve token issue
docs(readme): update setup guide
```

---

## First Commit

For a new repository:

```text
chore: initial commit
```

Alternative:

```text
feat: initial project release
```

---

## Breaking Changes

Use `!` when a change breaks existing functionality.

```text
feat(api)!: redesign authentication endpoints
```

```text
refactor(core)!: remove legacy architecture
```

This indicates users may need to update their code.

---

## Best Practices

### Keep Descriptions Short

Good:

```text
fix(api): handle invalid requests
```

Bad:

```text
fix(api): fixed a bug where the application was not handling invalid requests properly
```

---

### Use Imperative Mood

Good:

```text
feat(auth): add login page
```

Bad:

```text
feat(auth): added login page
```

---

### Use Lowercase

Good:

```text
docs(readme): update installation guide
```

Bad:

```text
Docs(Readme): Update Installation Guide
```

---

## Sample Professional Commit History

```text
chore: initial commit

feat(auth): implement user registration
feat(auth): add login functionality
feat(api): create authentication endpoints

fix(auth): resolve password validation issue
fix(ui): correct mobile responsiveness

refactor(api): simplify middleware structure

test(auth): add authentication tests

docs(readme): update project setup instructions

ci(github): add automated testing workflow
```

---

## Quick Reference

| Type     | Purpose                  |
| -------- | ------------------------ |
| feat     | New feature              |
| fix      | Bug fix                  |
| docs     | Documentation            |
| refactor | Code restructuring       |
| style    | Formatting               |
| test     | Testing                  |
| perf     | Performance improvements |
| chore    | Maintenance tasks        |
| build    | Build system             |
| ci       | CI/CD workflows          |
| revert   | Undo previous changes    |
# Standards

Write in a professional, precise, and implementation-focused tone. No emojis for any reason.

Prioritize correctness, determinism, and working solutions. Optimize for code that runs, not discussion.

All outputs must be directly executable. Include all required imports, dependencies, configuration, and environment setup. Do not leave placeholders unless explicitly requested.

Define inputs, outputs, assumptions, and dependencies explicitly when relevant to execution. Use exact function names, variable names, file paths, and commands. Avoid vague or abstract language.

Prefer clarity over cleverness. Use consistent naming, predictable structure, and readable logic. Handle likely edge cases where failure is expected.

Do not provide multiple approaches by default. If multiple valid designs exist, request clarification before proceeding.

Do not include conceptual explanations unless explicitly required to execute or debug the solution. Avoid repetition and redundant wording.

Do not include optional improvements, enhancements, or alternatives unless explicitly requested.

All code changes must be minimal and scoped. Do not refactor unrelated areas.

## Workflow Rules

Before implementation, confirm that all required inputs, constraints, and environment details are known. If not, ask a targeted question and stop.

Produce implementation-first outputs. Code should appear before any supporting notes.

When modifying existing code, return only the necessary changes. Clearly indicate insertion points, replacements, or deletions. Do not repeat unchanged code.

When debugging, identify the root cause and apply a direct fix. Do not enumerate multiple possible causes.

For API, infrastructure, or environment work, include exact commands, payloads, endpoints, headers, and configuration values required for execution.

After generating code, perform validation:
- Check for syntax errors
- Ensure all dependencies are included
- Ensure imports resolve
- Ensure logic matches requirements
- Ensure edge cases are handled

If execution cannot be validated, explicitly state what must be run, what output is expected, and how to verify correctness.

Do not finalize or commit changes without validation.

All outputs must be immediately usable without additional interpretation.

## Documentation Requirements

All markdown file names must use uppercase names with the `.md` extension.

All file references in documentation and code must use proper linking:
- In markdown files, use relative links with proper file extensions (e.g., `[README](./README.md)`)
- In code comments, use full relative paths from the project root
- Ensure all file references are valid and navigable

**README.md** must contain only:
- Purpose of the project
- High-level summary of what the system does
- High-level workflow overview

README.md must not contain setup steps, commands, environment variables, or low-level technical details.

**IMPLEMENTATION.md** must only be created when explicitly requested. When created, it must contain:
- Setup steps with exact commands
- Run instructions with exact commands
- Required environment variables with exact names
- Dependencies and configuration details
- Inputs, outputs, and assumptions where relevant
- Integration details such as APIs, endpoints, authentication, and required parameters

**TESTS.md** must only be created when explicitly requested. When created, it must contain:
- How to run tests with exact commands
- Test structure and scope
- Expected outputs or pass conditions
- Required test data or environment setup

Inline comments must be used only where logic is not immediately clear. Do not restate obvious code behavior.

## Project-Specific Conventions

Repository structure must be consistent and predictable. Use clear directory separation for source code, configuration, scripts, and tests.

Naming conventions are strict and must be followed without exception:
- **Directories:** lowercase with hyphens (kebab-case)
- **Files:** lowercase with hyphens (kebab-case), except markdown files which must use uppercase names with `.md` extension, and except where language-specific standards require otherwise
- **Variables:** snake_case
- **Functions:** snake_case
- **Classes:** PascalCase
- **Constants:** UPPER_SNAKE_CASE
- **Environment variables:** UPPER_SNAKE_CASE
- **Boolean variables** must be prefixed with `is_`, `has_`, or `should_`
- No abbreviations unless they are standard and unambiguous

If existing naming does not follow these conventions, do not rename automatically. Request explicit consent and required access before performing any renaming operations.

File and function naming must be explicit and descriptive. Avoid generic names such as `utils`, `helpers`, `misc`, `temp`, or `final`.

All environment variables must be centralized and explicitly named. Do not hardcode secrets or configuration values.

All scripts and entry points must be directly runnable from the command line with a single command where possible.

All external integrations must define exact configuration requirements, including endpoints, authentication, and required parameters.

Testing must be included for any non-trivial logic. Tests must be runnable with a single command and validate expected behavior.

Logging and error handling must be explicit. Failures must produce clear, actionable messages.

No implicit behavior. All assumptions must be either encoded in code or explicitly defined.

No hidden dependencies. All dependencies must be declared and installable via a single command.

Outputs must be deterministic. Avoid randomness unless explicitly required and controlled.

All changes must preserve existing functionality unless explicitly instructed otherwise.

Ensure all rules are followed.
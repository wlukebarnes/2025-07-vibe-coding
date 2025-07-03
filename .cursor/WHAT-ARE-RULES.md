# Cursor Rules

Cursor rules are configuration files that define how the Cursor AI assistant should behave when working in your codebase. They act as guidelines and constraints that help ensure consistent coding practices and project-specific requirements.

## What are Cursor Rules?

Cursor rules are typically defined in files like:

-   `.cursorrules/` - Main rules file for the project (deprecated)
-   `.cursor/rules/` Project-wide directory that contains various .mdc configuration files that apply to the entire project
-   `*/.cursor/rules/` For folder-scoped rules (e.g., ability to specify different rules for backend/ and frontend/)

## Common Rule Types

1. **Coding Standards** - Define formatting, naming conventions, and code style
2. **Technology Constraints** - Specify which frameworks, libraries, or tools to use/avoid
3. **Project Structure** - Define how files should be organized
4. **Security Guidelines** - Ensure safe coding practices
5. **Performance Requirements** - Set expectations for code efficiency

## Benefits

-   **Consistency** - Ensures all team members follow the same patterns
-   **Quality** - Enforces best practices and coding standards
-   **Efficiency** - Reduces time spent on code reviews and refactoring
-   **Maintainability** - Creates predictable, well-structured codebases

## Example Rules

```
- Use TypeScript for all new files
- Follow ESLint configuration
- Write unit tests for all functions
- Use descriptive variable names
- Keep functions under 50 lines
```

Cursor rules help the AI understand your project's specific needs and constraints, leading to more relevant and useful code suggestions.

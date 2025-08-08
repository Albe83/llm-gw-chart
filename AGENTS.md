# Guidelines for AI Agents

This document provides guidance for AI agents working in this repository.

## Development workflow
- Do not modify `AGENTS.md` unless explicitly requested.
- Use `rg` for searching; avoid commands like `grep -R` or `ls -R`.
- After modifying files, run all available tests with `pytest`. If other test suites are introduced, run them as well.
- When modifying the Helm chart, run `helm lint charts/llm-gateway` and ensure it succeeds. If linting fails, identify and fix the issue, then rerun the command until it passes.
- For Helm chart development, define default values for variables in the `values.yaml` file unless explicitly requested otherwise or when implementation constraints make it technically infeasible.
- When modifying Helm charts, update `values.schema.json` to cover every variable used. Ensure the schema is complete, syntactically valid, and includes both validation rules and metadata documenting each value's behavior and effects.
- Unless explicitly instructed otherwise, adhere to Helm.sh and Kubernetes best practices when developing or modifying charts.
- Keep commits focused and descriptive, using the present tense (e.g., "Add feature" rather than "Added feature").

## Code style
- Maintain consistent formatting with any tools configured in the repository. If formatting tools (such as `black` or `pre-commit`) are available, run them before committing.
- Write code—including Helm templates and configuration—with a clear and readable style so that even less-experienced contributors can understand it.
- Take inspiration from the style used in Bitnami charts, but avoid introducing dependencies on external charts unless explicitly requested.
## Documentation
- Use English for all documentation, comments, and notes.
- Comment critical sections of code to explain their purpose and rationale; where helpful, note other areas of the code that a change may impact.
- Update documentation or comments when behavior changes or new features are introduced.
- Prefer Markdown as the format for documentation artifacts.

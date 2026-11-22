# Security Policy

## Supported versions

Only the latest version on the `main` branch is supported with security fixes.

## Reporting a vulnerability

Do not open a public issue for security problems.

Report privately through GitHub: go to the repository's **Security** tab and choose **Report a vulnerability**.

Include:

- A description of the problem and its impact.
- Steps to reproduce, or a minimal example input.
- The affected file or section (for example, a rule in `SKILL.md`).

We aim to acknowledge reports within a reasonable time and will keep you informed of progress. We ask that you give us a chance to fix the issue before public disclosure.

## Scope

This project is a Markdown instruction file (`SKILL.md`). Relevant risks include:

- Prompt injection through text inside images that changes the skill's behavior, skips flags, or alters the output.
- Spreadsheet formula injection in generated files (for example, a cell starting with `=` that runs a formula).
- Instructions that cause an AI to leak private stock or document data, or run unsafe actions.

Reports in these areas are welcome.

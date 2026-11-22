# Contributing

Thanks for helping improve stock-count-transcribe.

## Scope

The project is one skill: `SKILL.md`. Changes must keep it:

- **Tool-agnostic.** No instructions tied to a single AI product, IDE, or tool name. The skill must work when pasted into any AI assistant that accepts images.
- **Self-contained.** All behavior lives in `SKILL.md`. Do not add scripts, dependencies, or required setup.
- **Written in English.** The skill body is English. The output it produces is neutral Latin American Spanish (es-419), and that rule must stay.

Out of scope: output in other languages by default, regional Spanish (voseo, country-specific slang), delivery notes or invoices (see paper-to-spreadsheet), reconciliation against stock systems, and features that only work in one tool.

## Before you open a pull request

1. Open an issue first for anything beyond a typo or a clear bug fix.
2. Keep the diff small. One change per pull request.
3. Test the change with at least two inputs (see below) and check that:
   - Every visible row is transcribed, in order, with no invented rows.
   - Illegible, crossed-out, ambiguous, or blank values are flagged (yellow cell, comment, and `Revisar` sheet, or the CSV/TSV Revisar block), not guessed.
   - Blank quantities stay empty, not 0.
   - Totals use formulas, cover only the intended columns, and the note counts the values left out.
   - Output is es-419, with default es-AR number format, and the header is on the first line.
   - The skill asks for a new photo when no image can be read, and asks when the image is not a stock count.
4. Update `README.md` if install or usage changes.

## Examples and test inputs

- Use invented locations, products, codes, and numbers. Never include real customer, supplier, company, or personal data, including in photos.
- Do not commit secrets, tokens, or private documents.
- Suggested test set: one printed stock sheet with a clean table and two locations (two photos), and one handwritten notebook page with a crossed-out value, a blank quantity, and an unclear digit.

## Pull request description

Include:

- What changed and why.
- The test inputs you used and the output you got.
- Any rule in `SKILL.md` you changed, and the reason.

## Commit messages

- Short imperative subject line, under 72 characters. Example: `Leave blank quantities empty in count totals`.
- Body optional, for context.

## License

By contributing, you agree that your contribution is licensed under the MIT License in [LICENSE](LICENSE).

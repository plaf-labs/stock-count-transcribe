# stock-count-transcribe — turn photos of a stock count into an Excel-ready table (Spanish)

Turn photos of a physical stock count (printed sheet, handwritten notebook, or whiteboard) into a count table ready for Excel. It transcribes what is written, flags what is doubtful, and never fills gaps with guesses.

Works with any AI assistant that accepts images.

## Who it is for

Small and mid-size warehouses or workshops that count stock on paper and need the count in a spreadsheet.

## What it does

- Reads one or more photos, one per location or aisle.
- Keeps the source columns, or uses a default set when there is no header.
- Transcribes rows in order, with no invented data.
- Marks illegible, crossed-out, ambiguous, or blank values in yellow cells with a comment, and lists them in a `Revisar` sheet.
- Computes totals with formulas and notes how many values the total leaves out.
- Outputs .xlsx, or CSV or TSV if files cannot be created. Numbers use es-AR format by default (decimal comma).

## What it does not do

- It does not replace your stock system and does not reconcile counts with system balances.
- It does not verify quantities against the physical stock. A person must review flagged rows and spot-check the count.
- It does not store data between sessions.
- It is not for delivery notes or invoices. Use paper-to-spreadsheet for those.

## Install

`SKILL.md` is the only file the AI needs. It is plain Markdown with no tool-specific dependencies.

Paste the contents of `SKILL.md` as the system prompt, custom instructions, or first message, or put it wherever your tool reads project instructions.

## Usage

Attach the photos and write:

```
Convertí estos conteos en una planilla para Excel. Son dos fotos: Foto 1 es Depósito A, Foto 2 es Depósito B.
```

If no location is given and the photos do not show one, the skill leaves Ubicación empty and flags those rows.

## Adapting

- Default columns: edit the "Steps" section of `SKILL.md`.
- Number format: change the "Output format" section (default es-AR).
- Output language: change the es-419 rule in "Output format".

## Example

See the synthetic example in `SKILL.md`, section "Example".

## License

MIT. See [LICENSE](LICENSE).

---

Made by [PLAF Labs](https://github.com/plaf-labs) · Software, automation and web development for SMEs and industrial companies · [plaf.agency](https://plaf.agency)

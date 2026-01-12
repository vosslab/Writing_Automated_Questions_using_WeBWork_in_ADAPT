# Plan

This README is the working plan for expanding the chapter-based guide in `Textbook/` using
source material from `Insight-HTML/` and `WebWorK-HTML/`. The guide stays focused on science
and descriptive fields, reflecting Neil Voss's emphasis on applied domains.

## Requirements
- Use `Insight-HTML/` and `WebWorK-HTML/` as source material only; do not modify the archives.
- Expand the chapter structure inside `Textbook/` rather than inventing new top-level folders.
- Keep the tone and examples focused on science and descriptive fields.
- Maintain HTML pages as the primary chapter format.
- Record edits in `docs/CHANGELOG.md`.

## Scope
- In: add chapter index content, create or expand subchapter HTML files, and include worked
  examples and checklists.
- Out: reorganizing the source archives, creating new platforms, or rewriting the guide as a
  different format.

## Files and entry points
- `Textbook/01_Introduction/1.0-Index.html`
- `Textbook/01_Introduction/1.5-Quickstart_copy_edit_first_problem.html`
- `Textbook/02_Problem_Generation_PG/2.0-Index.html`
- `Textbook/03_PGML_PG_Markup_Language/3.0-Index.html`
- `Textbook/04_Simple_Problem_Example_in_WeBWorK/4.0-Index.html`
- `Textbook/05_Question_Types/5.0-Index.html`
- `Textbook/06_WeBWorK_for_Different_Subjects/6.0-Index.html`
- `Textbook/07_ADAPT_Workflow/7.0-Index.html`
- `Textbook/08_Debugging_and_QA/8.0-Index.html`
- `Textbook/09_Randomization_and_Reproducibility/9.0-Index.html`
- `Textbook/10_Answer_Checking_for_Science/10.0-Index.html`
- `Textbook/11_Accessibility_and_Clarity/11.0-Index.html`
- `Textbook/12_Maintenance_and_Sharing/12.0-Index.html`
- `Textbook/90_Appendices/90.0-Index.html`
- `Insight-HTML/`
- `WebWorK-HTML/`
- `docs/CHANGELOG.md`

## Chapter expansion map
- 01 Introduction: WeBWorK overview, why use it in sciences, key features, and how ADAPT fits.
- 02 Problem generation (PG): PG file structure, common macros, randomization, and contexts.
- 03 PGML: syntax, formatting, answer blanks, math notation, tables, images, and links.
- 04 Simple example: end-to-end walkthrough with PG and PGML for a science-flavored question.
- 05 Question types: design patterns (MC, matching, numeric entry, blanks, ordering).
- 06 Different subjects: domain patterns, pitfalls, and examples (biology, chemistry, etc.).
- 07 ADAPT workflow: authoring, cloning, assignment building, QA, and publishing.
- 08 Debugging and QA: previewing, error patterns, variant testing, and student-view pitfalls.
- 09 Randomization and reproducibility: seeds, constraints, and stable reporting rules.
- 10 Answer checking for science: tolerances, units, reporting conventions, misconceptions.
- 11 Accessibility and clarity: ESL-friendly prompts, ambiguity traps, basic accessibility.
- 12 Maintenance and sharing: naming, reuse across terms, versioning, licensing hygiene.
- 90 Appendices: templates, cheat sheets, glossary, troubleshooting.

## Action items
[ ] Audit `Insight-HTML/` and `WebWorK-HTML/` for the best source pages per chapter.
[ ] Draft or expand each chapter index with a short intro and a section outline.
[ ] Create subchapter HTML files for new sections, using consistent naming and numbering.
[ ] Add worked examples and checklists that prioritize science and descriptive contexts.
[ ] Avoid HTML links in textbook content (LibreTexts provides its own TOC).
[ ] Review for tone, clarity, and consistency with the chapter progression.

## Testing and validation
- Open a sample of updated HTML files in a browser to confirm formatting and rendering.
- Verify chapter numbering and file naming consistency across `Textbook/`.
- Run `tests/run_html_lint.sh`.

## Risks and edge cases
- Source content may conflict across Insight and WebWorK pages; resolve with a clear stance.
- Overemphasis on math examples can dilute the science focus.
- Licensing references must remain accurate when quoting or adapting content.

## Open questions
- Do you want each chapter to end with a short summary and exercises section?
- Should examples favor biology and chemistry first, or be evenly distributed by field?

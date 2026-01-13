## Coding Style
See Python coding style in docs/PYTHON_STYLE.md.
See Markdown style in docs/MARKDOWN_STYLE.md.
See repo style in docs/REPO_STYLE.md.
When making edits, document them in docs/CHANGELOG.md.
When in doubt, implement the changes the user asked for rather than waiting for a response; the user is not the best reader and will likely miss your request and then be confused why it was not implemented or fixed.
When changing code always run tests, documentation does not require tests.
Agents may run programs in the tests folder, including smoke tests and pyflakes/mypy runner scripts.

## Project intent (read this first)
This repo is primarily a textbook/guide in the `Textbook/` folder, not a traditional software
project. Most work is writing and editing HTML chapter content that will be imported into
LibreTexts.

### Authoring constraints for `Textbook/`
- External HTML links (`<a href=...>`) are allowed in textbook content. Do not link to other
  sections/pages of this textbook; LibreTexts provides its own TOC and internal links are likely to
  break.
- The textbook cannot rely on JavaScript; do not add `<script>` tags or inline event handlers.
- Prefer PGML-focused writing; regular PG authoring is discouraged except for minimal setup.

### Content examples
Use the style of science prompts and structured data from the Biology Problems OER as a guide
when creating examples:
- `/Users/vosslab/nsh/biology-problems/`
- `/Users/vosslab/nsh/biology-problems-website/`

### Linting HTML
Run the local HTML lint checker when editing textbook HTML:
- `tests/run_html_lint.sh`

## Environment
Codex must run Python using `/opt/homebrew/opt/python@3.12/bin/python3.12` (use Python 3.12 only).
On this user's macOS (Homebrew Python 3.12), Python modules are installed to `/opt/homebrew/lib/python3.12/site-packages/`.

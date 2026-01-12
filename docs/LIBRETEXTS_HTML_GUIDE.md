# LibreTexts HTML guide

This doc captures the minimal HTML patterns to use in `Textbook/` so the content imports cleanly
into LibreTexts and remains maintainable.

## Core rules
- Do not add HTML links (`<a href=...>`) in textbook content; LibreTexts provides its own TOC and
  links are likely to break.
- Do not use JavaScript; avoid `<script>` tags and inline event handler attributes (like
  `onclick=`).
- Prefer simple, semantic HTML: `p`, `h2`, `h3`, `ul`, `ol`, `li`, `code`, `pre`, and tables for
  real tabular data.

## Index pages (X.0-Index.html)
Every chapter index page named like `X.0-Index.html` must end with this line so LibreTexts shows
the generated list of subsections:

```html
<p>{{template.ShowOrg()}}</p>
```

## Tables (the standard format)
Use LibreTexts responsive tables so the content remains readable on narrow screens and accessible
to assistive technologies.

### Requirements
- Use `class="mt-responsive-table"` on the `<table>`.
- Use `<thead>` and `<tbody>`.
- In each `<td>`, include a `data-th="Header name"` attribute matching the column header text.
- Prefer a `<colgroup>` with explicit widths when you want consistent column sizing.
- Do not use `border=`, `cellpadding=`, or `cellspacing=` attributes.

### Template
```html
<table class="mt-responsive-table">
	<colgroup>
		<col style="width: 22%;">
		<col style="width: 39%;">
		<col style="width: 39%;">
	</colgroup>
	<thead>
		<tr>
			<th>Format</th>
			<th>Best for</th>
			<th>Tradeoffs</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td data-th="Format">WeBWorK (PGML-first)</td>
			<td data-th="Best for">...</td>
			<td data-th="Tradeoffs">...</td>
		</tr>
	</tbody>
</table>
```

## Validation
- Run `tests/run_html_lint.sh` after editing textbook HTML.

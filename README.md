# Assignment Template

Quarto template for academic assignments in Brazilian Portuguese. Includes a custom `assignment-pdf` format extension with pre-configured LaTeX headers for proper Portuguese typesetting, clean page layout, and code highlighting.

## Usage

```bash
quarto use template guilhermemarthe/assignment-template
```

This will create a new directory with the template files. Edit `template.qmd` and render:

```bash
quarto render template.qmd
```

## Format: `assignment-pdf`

The `assignment-pdf` format bundles:

- **XeLaTeX** with `polyglossia` for Brazilian Portuguese
- **fancyhdr** header: title, author, and date in a single line
- **GitHub-style** code highlighting with light gray background
- Tight page margins and `H` float placement for figures
- Heading level shift (+2) so `##` renders as the top visible heading

Override any setting in your document front matter:

```yaml
format:
  assignment-pdf:
    keep-tex: true
    geometry:
      - top=1in
```

## Dependencies

- [Quarto](https://quarto.org) >= 1.4.0
- A TeX distribution with XeLaTeX (e.g., TeX Live, TinyTeX)
- Python 3 with Jupyter (for `.qmd` code cells)

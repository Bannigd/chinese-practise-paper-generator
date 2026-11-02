# Chinese Practice Grid Generator

Offline generator of Chinese handwriting practice sheets: mi-zi-ge (米字格),
tian-zi-ge (田字格), or an empty grid. One HTML file, no dependencies, no internet.

[Русский](README.ru.md)

## Usage

1. Open `index.html` in a browser.
2. Adjust the cell size, margins, and inner guides.
3. Click **Print / PDF**, then choose **Save as PDF** with margins **None** and scale **100%**.
4. Or click **Download SVG** to save a vector template.

The **RU / EN** switch in the top-right corner changes the interface language.
Use `?lang=en` or `?lang=ru` in the URL to force it.

## Command line

```bash
google-chrome --headless --no-pdf-header-footer \
  --print-to-pdf=chinese-grid.pdf \
  "file://$(pwd)/index.html?cell=16&margin=14&guides=mizige&format=a4&lang=en"
```

`guides`: `mizige`, `tianzige`, `diagonals`, `none`. `format`: `a4`, `a5`, `letter`.
`lang`: `en`, `ru`. Other settings match the UI.

`$(pwd)` must point to the directory with `index.html`; a literal placeholder path
causes `ERR_FILE_NOT_FOUND`.

## Example

[`example-16mm-a4.pdf`](example-16mm-a4.pdf) ·
[`example-16mm-a4-ru.pdf`](example-16mm-a4-ru.pdf)

# HTML5 Program Examples

A collection of **20 small, standalone HTML5 pages**, each demonstrating one element or feature of HTML5: semantic layout tags, form input types, media elements, graphics and a few interactive widgets. Most files include comments explaining what the element is for, which attributes it accepts and how to use it well. There is no build step, framework or backend, so every example runs by opening the file in a browser.

## Examples

### Semantic structure

| File | Element | What it shows |
| --- | --- | --- |
| `layout.html` | `<header>`, `<nav>`, `<main>`, `<footer>` | Basic semantic page skeleton with placeholder content |
| `section.html` | `<section>` | Four thematic sections followed by a footer |
| `article.html` | `<article>` | Four self-contained article blocks, each with a heading |
| `aside.html` | `<aside>` | A sidebar-style group of radio buttons (Men, Women, Kids, Girls, Home Decor) |

### Text and content

| File | Element | What it shows |
| --- | --- | --- |
| `blockquote.html` | `<blockquote>` | A block quotation with a `cite` attribute |
| `code.html` | `<code>` | Inline code styled with CSS |
| `mark.html` | `<mark>` | Highlighting a word inside a paragraph |
| `bdo-tag.html` | `<bdo>` | Overriding text direction with `dir="rtl"` |
| `wbr.html` | `<wbr>` | Word-break opportunities inside very long words |
| `figure-figcaption.html` | `<figure>`, `<figcaption>` | An image with a caption |

### Interactive elements and forms

| File | Element | What it shows |
| --- | --- | --- |
| `form.html` | HTML5 input types | `color`, `date`, `month`, `range`, `number`, `image`, `hidden`, `tel`, `search` and a submit button |
| `datalist.html` | `<datalist>` | A text input with city suggestions (Pune, Nashik, Satara, Solapur) |
| `details.html` | `<details>`, `<summary>` | An expandable "Copyright Information" disclosure |
| `dialog.html` | `<dialog>` | A native dialog box shown with the `open` attribute |
| `meter.html` | `<meter>` | A gauge showing 25 on a scale of 0 to 100 |
| `progres.html` | `<progress>` | A progress bar showing 35 out of 200 |

### Media and graphics

| File | Element | What it shows |
| --- | --- | --- |
| `audio.html` | `<audio>` | Audio player with `controls`, `loop`, `autoplay` and `muted`, plus fallback content |
| `vedio.html` | `<video>` | Video player with `controls`, `autoplay`, `loop` and `muted`, plus notes on `<source>` and captions |
| `canvas.html` | `<canvas>` | A 300×300 canvas whose background turns red when a button is clicked |
| `svg.html` | Inline `<svg>` | A circle, a gradient blob and a wave shape |

## Project Structure

```
HTML_5-program/
├── article.html, aside.html, audio.html, bdo-tag.html, blockquote.html,
│   canvas.html, code.html, datalist.html, details.html, dialog.html,
│   figure-figcaption.html, form.html, layout.html, mark.html, meter.html,
│   progres.html, section.html, svg.html, vedio.html, wbr.html
└── assets/             # Media used by the examples
    ├── background1.jpeg
    ├── song.mp4
    └── Armaan_Malik_-_Control_(Official_Video)(128k).m4a
```

## Getting Started

### Prerequisites

A modern web browser. No other tools or internet connection are needed.

### Run locally

1. Clone the repository:
   ```bash
   git clone https://github.com/AmanPatil2002/HTML_5-program.git
   cd HTML_5-program
   ```
2. Open any `.html` file in your browser, or serve the folder with a static server:
   ```bash
   npx serve .
   ```
   Keep the files in the same folder as `assets/`, because `audio.html`, `vedio.html` and `figure-figcaption.html` load media from it.

## Notes and Known Limitations

- **Media in the repository:** `assets/` contains a commercial song video and audio track (`song.mp4` and the `.m4a` file). If the repository is public, consider replacing them with your own or royalty-free media.
- **Autoplay:** `audio.html` and `vedio.html` start muted because browsers block autoplay with sound. Use the player controls to unmute.
- **`form.html`:** `type="date-time"` is not a valid input type, so the browser shows a plain text box. Use `datetime-local` instead. The `image` input has no `src`, none of the fields have a `name`, and the labels are not linked to their inputs, so submitting the form sends no data.
- **`datalist.html`:** `type="city"` is not a valid input type (it falls back to text), and the preset value "Select City" hides the suggestions until you clear the box. Use `placeholder` instead of `value`.
- **`blockquote.html`:** the explanatory comment is wrapped in Django-style `{% comment %}` tags instead of an HTML comment, so that text appears on the page. Replace it with `<!-- ... -->`.
- **`canvas.html`:** the button only changes the CSS background color. It does not draw with the canvas 2D API, and the `width`/`height` attributes should be plain numbers (`300`), not `300px`.
- **`wbr.html`:** it has a closing `</p>` without an opening `<p>`.
- **`layout.html`:** the `<img>` and `<nav>` elements are empty placeholders.
- **`article.html`:** the viewport meta tag reads `width=<device-width>`; it should be `width=device-width`.
- Most pages still use the default title "Document", and two file names contain typos (`progres.html` and `vedio.html`).

## Author

**Aman Patil** – [@AmanPatil2002](https://github.com/AmanPatil2002)

## License

This repository is for learning and practice purposes. Add a license of your choice if you plan to share or reuse it.

# Angles of Angel

A single-page portfolio website for showcasing art pieces. Built with plain HTML, CSS and JavaScript, with no frameworks, build tools or dependencies.

## Features

- **Header** with the site title
- **About me** section with a portrait and short biography
- **Gallery grid** with 3 tiles per row on desktop (2 on tablets, 1 on phones)
- **Lightbox viewer**: click any piece to see it larger, click again to close
- **Contact footer** with email, phone, social and studio location
- **Automatic fallback**: if an image file is missing, a placeholder is shown instead
- **Responsive and accessible**: keyboard focus styles, descriptive alt text and reduced-motion support

## Project structure

```
your-folder/
├── angles-of-angel.html    # the whole site: HTML, CSS and JS in one file
├── images/
│   ├── portrait.jpg        # optional, shown in the About section
│   ├── art1.jpeg
│   ├── art2.jpeg
│   └── ...
└── README.md
```

## Getting started

1. Keep `angles-of-angel.html` and the `images` folder side by side.
2. Open `angles-of-angel.html` in any modern browser (double-click it).

No installation or server is needed.

## Customisation

### Adding or changing artwork

Open `angles-of-angel.html` and find the `pieces` list near the bottom, inside the `<script>` block:

```js
const pieces = [
  {title:"Fold I",  note:"Acrylic on canvas, 2026", file:"art1.jpeg"},
  {title:"Fold II", note:"Acrylic on canvas, 2026", file:"art2.jpeg"}
];
```

| Field   | Description                                              |
|---------|----------------------------------------------------------|
| `title` | Name of the piece, shown under the image                 |
| `note`  | Medium, year or any short description                    |
| `file`  | Image file name inside the `images` folder (case-sensitive) |

Add, remove or reorder entries as needed. The grid adjusts automatically.

### Portrait

Set `PORTRAIT_FILE` to your photo's file name (default: `portrait.jpg`).

### Text and contact details

Edit the "About me" paragraphs and the contact list directly in the HTML body. Replace the placeholder email, phone number, Instagram link and studio location with your own.

### Colours

Colours are defined as variables at the top of the `<style>` block:

```css
:root{
  --bg:#d5b1e3;    /* page background */
  --ink:#111B33;   /* main text */
  --muted:#33304F; /* secondary text */
  --accent:#0e1753;/* accents and focus outline */
  --tile:#e6d0ef;  /* image tile background */
  --foot:#c39ad6;  /* footer background */
  --foot-ink:#111B33; /* footer text */
}
```

### Fonts

The site uses [Syne](https://fonts.google.com/specimen/Syne) and [Karla](https://fonts.google.com/specimen/Karla) from Google Fonts. Offline, it falls back to the system font.

## Image tips

- Square images work best, since tiles are cropped to a 1:1 ratio.
- Use JPEG or WebP, ideally under 500 KB each, for fast loading.
- Avoid spaces and special characters in file names, for example `fold-1.jpg`.

## Browser support

Works in current versions of Chrome, Edge, Firefox and Safari.

## Deployment

Because the site is a static page, it can be hosted anywhere. Upload the HTML file and the `images` folder together to a service such as GitHub Pages, Netlify or Cloudflare Pages.

## License

All artwork and content &copy; Angles of Angel. All rights reserved.

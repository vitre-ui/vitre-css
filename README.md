# Vitre CSS

The transparent style layer. Classless CSS with a high-end finish. Clear. Light. Vitre.

Vitre CSS is a single-file CSS library for making raw semantic HTML look polished by default. Drop in `vitre.css` and ordinary elements such as headings, links, buttons, forms, tables, code blocks, dialogs, and details receive modern light and dark theme styling without required classes.

## Install

Use the file directly:

```html
<link rel="stylesheet" href="vitre.css">
```

Install from npm:

```sh
npm install vitre-css
```

Use a CDN after publishing:

```html
<link rel="stylesheet" href="https://unpkg.com/vitre-css/vitre.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/vitre-css/vitre.css">
```

## Documentation

The documentation site is hosted with GitHub Pages:

```text
https://appurist.github.io/vitre-css/
```

The npm package metadata uses this URL as its `homepage`, so npmjs.org links to the GitHub-hosted documentation site.

The Pages source is `docs/index.html`. In the GitHub repository settings, enable Pages from the `main` branch and `/docs` folder. The docs site uses `docs/vitre.css`; run `npm run sync:docs` after changing the root stylesheet.

## Usage

Write semantic HTML and let Vitre style the elements directly:

```html
<main>
  <section>
    <h1>Account settings</h1>
    <p>Manage your profile and notification preferences.</p>

    <form>
      <label>
        Email
        <input type="email" placeholder="you@example.com">
      </label>

      <button>Save changes</button>
    </form>
  </section>
</main>
```

## Themes

Vitre follows the user's operating system preference by default with `prefers-color-scheme`. You can force a theme with `data-theme` on the root element:

```html
<html data-theme="dark">
```

Supported values are `light` and `dark`.

## Customization

The main customization API is CSS variables. Override `--vitre-*` properties after importing Vitre:

```css
:root {
  --vitre-hue: 168;
  --vitre-primary: hsl(var(--vitre-hue) 76% 42%);
  --vitre-radius: 0.5rem;
  --vitre-measure: 80ch;
}
```

Useful tokens include colors, spacing, typography, surfaces, borders, focus rings, forms, tables, shadows, and code blocks. See `vitre.css` for the full variable surface.

## What It Styles

- Page layout primitives: `body`, `header`, `main`, `section`, `article`, `aside`, `footer`, and `nav`
- Typography: headings, paragraphs, links, lists, blockquotes, `mark`, `small`, and horizontal rules
- Code: `code`, `pre`, `kbd`, and `samp`
- Forms: labels, buttons, inputs, textareas, selects, fieldsets, checkboxes, radios, ranges, and color inputs
- Data and disclosure: tables, `details`, `summary`, `dialog`, `progress`, and `meter`
- Media: images, videos, SVGs, canvas, and iframes

## Browser Support

Vitre targets modern browsers and uses current CSS features including cascade layers, `color-mix()`, `:where()`, `:has()`, logical properties, `clamp()`, and `backdrop-filter`. It favors a small, expressive stylesheet over legacy fallbacks.

## Visual Test Page

Open `test.html` directly or the `docs` folder in a browser to check the visual look and feel across common semantic elements. It only depends on the local `vitre.css` file.

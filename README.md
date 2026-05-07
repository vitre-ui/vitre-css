# Vitre CSS

The transparent style layer. Classless CSS with a high-end finish. Clear. Light. Vitre.

A great looking web page without any `class="..."` or `style="..."` on your HTML elements. Just add `<link rel="stylesheet" href="vitre.css">` (or equivalent) and you're done.

Vitre CSS is a single-file CSS library for making raw semantic HTML look polished by default. It honors semantic tags without polluting markup, so ordinary elements such as headings, links, buttons, forms, tables, code blocks, dialogs, and details receive modern light and dark theme styling without required classes.

## Related
Work has begun on a related but opposite project, [vitre-js](https://www.npmjs.com/package/vitre-js): styleless interactivity for semantic components. Use either package on its own, or pair them when you want Vitre styling and Vitre behavior together.

## Links

- GitHub docs: https://appurist.github.io/vitre-css/
- GitHub repo: https://github.com/appurist/vitre-css
- npmjs.org: https://www.npmjs.com/package/vitre-css
- vitre-js: https://www.npmjs.com/package/vitre-js


## Install

Use the file directly:

```html
<link rel="stylesheet" href="vitre.css">
```

Install from npm:

```sh
npm install vitre-css
```

Use a CDN:

```html
<link rel="stylesheet" href="https://unpkg.com/vitre-css/vitre.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/vitre-css/vitre.css">
```

## Documentation

Read the [documentation and examples](https://appurist.github.io/vitre-css/).

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

The main customization API is CSS variables. Add your own stylesheet after Vitre and override `--vitre-*` values there:

```html
<link rel="stylesheet" href="vitre.css">
<link rel="stylesheet" href="custom.css">
```

In `custom.css`, start with variable overrides:

```css
:root {
  --vitre-hue: 168;
  --vitre-primary: hsl(var(--vitre-hue) 76% 42%);
  --vitre-font-weight: 400;
  --vitre-radius: 0.5rem;
  --vitre-measure: 80ch;
  --vitre-button-height: 40px;
  --vitre-button-bg-angle: 180deg;
}
```

Useful tokens include colors, spacing, typography, surfaces, borders, focus rings, forms, tables, shadows, and code blocks. See `vitre.css` for the full variable surface.

Buttons expose background and hover variables. Use `data-variant` for common button treatments:

```css
:root {
  --vitre-button-bg-image: none;
}
```

For a single flat button, use the variant attribute instead of adding a class:

```html
<button type="button" data-variant="flat">Flat button</button>
```

Other supported variants are `outline`, `ghost`, and `plain`:

```html
<button type="button" data-variant="outline">Outline button</button>
<button type="button" data-variant="ghost">Ghost button</button>
<button type="button" data-variant="plain">Plain button</button>
```

Token swatches can use `data-token`:

```html
<mark data-token="primary"></mark>
<mark data-token="surface"></mark>
```

If a selector does not expose the exact customization you need, override the element rule in your stylesheet after Vitre:

```css
button {
  text-transform: none;
}
```

Prefer variables when they exist. If you find yourself repeatedly overriding the same kind of rule, that is a good sign Vitre should expose another `--vitre-*` variable for that customization.

## What It Styles

- Page layout primitives: `body`, `header`, `main`, `section`, `article`, `aside`, `footer`, and `nav`
- Typography: headings, paragraphs, links, lists, blockquotes, `mark`, `small`, and horizontal rules
- Code: `code`, `pre`, `kbd`, and `samp`
- Forms: labels, buttons, inputs, textareas, selects, fieldsets, checkboxes, radios, ranges, and color inputs
- Data and disclosure: tables, `details`, `summary`, `dialog`, `progress`, and `meter`
- Data patterns: `[data-kind="alert"]`, `[data-color="warning"]`, `[role="dialog"]`, and grouped form controls
- Media: images, videos, SVGs, canvas, and iframes

## Browser Support

Vitre targets modern browsers and uses current CSS features including cascade layers, `color-mix()`, `:where()`, `:has()`, logical properties, `clamp()`, and `backdrop-filter`. It favors a small, expressive stylesheet over legacy fallbacks.

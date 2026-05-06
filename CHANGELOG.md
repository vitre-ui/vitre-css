# Changelog

## 1.2.0 - 2026-05-06

- Split theme palette variables into `vitre.light` and `vitre.dark` cascade layers while keeping shared variables in `vitre.theme`.
- Refactored `color-mix()` usage into named dependent variables so generated colors remain overrideable.
- Added explicit spacing between adjacent card-rendered semantic panels, including document sections, articles, asides, and nested section articles.
- Replaced blank kitchen sink media placeholders with local MP3 and MP4 examples, a YouTube iframe embed, and live object/embed examples.

## 1.1.1 - 2026-05-03

- Added explicit spacing between adjacent card-rendered semantic panels, including document sections, articles, asides, and nested section articles.
- Split theme palette variables into `vitre.light` and `vitre.dark` cascade layers while keeping shared variables in `vitre.theme`.
- Replaced blank kitchen sink media placeholders with local MP3 and MP4 examples, a YouTube iframe embed, and live object/embed examples.
- Refactored `color-mix()` usage into named dependent variables so generated colors remain overrideable.

## 1.1.0 - 2026-05-03

- Added nested semantic structure styling for article cards with direct header and footer regions.
- Added card treatment for articles nested inside main or section content.
- Added nested aside callouts for supplementary content inside articles and sections.
- Added definition-list term and description styling for `dt` and `dd`.
- Added role-based banner styling for `[role="alert"]`, `[role="status"]`, and `[role="note"]` with dedicated `--vitre-alert-*`, `--vitre-status-*`, and `--vitre-note-*` variables.
- Added neutral styling for `dialog > article` so native dialog content can use semantic article structure without duplicate panel chrome.
- Expanded the kitchen sink page and docs coverage summary for the new semantic structure patterns.

## 1.0.2 - 2026-05-03

- Added explicit styling for additional semantic HTML elements, including captions, table footers, abbreviations, addresses, timestamps, inserted and deleted text, subscript and superscript text, outputs, embedded media, search regions, menus, heading groups, and ruby annotations.
- Added `--vitre-inserted`, `--vitre-inserted-bg`, `--vitre-deleted`, and `--vitre-deleted-bg` tokens for document-change styling.
- Expanded the kitchen sink page with examples for the new element coverage.
- Updated the documentation element coverage summary and kept the GitHub Pages stylesheet copy in sync.

## 1.0.1 - 2026-05-01

- Added native form validation styling for `:user-invalid` and `:user-valid` using existing semantic color variables.
- Added `[aria-busy="true"]` button styling with a CSS-only spinner and `--vitre-busy-*` customization variables.
- Improved `progress` styling with explicit native bar colors and rounded shape.
- Updated the CSS banner version to match the package version.
- Removed the old concept document from the npm package and folded its user-facing positioning into the README.
- Kept the GitHub Pages stylesheet copy in sync with the package stylesheet.

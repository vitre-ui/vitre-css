# Repository Guidelines

## Project Structure & Module Organization
This repository is currently documentation-first. The main source of truth is [VitreCSS.md](/C:/dev/appurist/vitre-css/VitreCSS.md), which defines the Vitre design goals, CSS token ideas, and planned styling work.

Keep new files grouped by purpose as the project grows:
- `VitreCSS.md` for product and styling documentation
- `src/` for the CSS library source
- `examples/` for raw HTML demos
- `tests/` for visual or automated checks

Prefer small, focused files. Example: `src/tokens.css`, `src/forms.css`, `examples/forms.html`.

## Build, Test, and Development Commands
There is no build system checked in yet. Until one exists, contributors should validate changes by editing Markdown directly and previewing rendered HTML/CSS locally.

Common local commands:
- `Get-Content -Raw VitreCSS.md` to inspect the current spec from the terminal
- `rg "vitre-"` to find token names and keep variables consistent

If a toolchain is added later, document the exact commands here and in the README at the same time.

## Coding Style & Naming Conventions
Use 2-space indentation in CSS and Markdown examples. Keep CSS classless by default: style semantic elements first, then introduce utility or opt-in classes only when element selectors are insufficient.

Naming guidance:
- CSS custom properties: `--vitre-*`
- File names: lowercase with hyphens, such as `code-blocks.css`
- Headings and checklist items in docs should be concise and action-oriented

## Testing Guidelines
No automated tests are present yet. For CSS changes, include a minimal HTML example that demonstrates the affected element states, such as default, hover, and focus.

When tests are introduced, place them under `tests/` and name files after the feature they cover, for example `tests/buttons.html` or `tests/tokens.spec.*`.

## Commit & Pull Request Guidelines
Git history is not available in this workspace, so use a simple imperative commit style: `Add table styling spec` or `Refine glass token names`.

Pull requests should include:
- A short summary of the change
- Any updated example or screenshot for visual changes
- Notes on new tokens, selectors, or breaking styling decisions

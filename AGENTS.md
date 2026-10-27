# AGENTS.md

Source of truth for all AI agents working in this repo. Keep it current when conventions change.

## What this is

Automation Practice Ground: a static web playground for practicing test automation (Selenium, Playwright, Cypress, etc.), inspired by *the-internet*. Each page is a self-contained scenario with deliberate automation challenges.

## Stack

- Vanilla HTML5, CSS3, and JavaScript only. No framework, no bundler, no package manager, no build step, no tests.
- Do not add dependencies or tooling unless explicitly asked.
- External requests: Google Fonts (Inter, Fira Code) only.

## Deployment

Hosted on GitHub Pages from `master` (root): https://farizagati.github.io/web-automation-practice-ground/. Keep links relative; no server-side features.

## Layout

```
index.html        Homepage: hero + scenario list (ul#scenario-list)
styles.css        Single shared stylesheet (design tokens in :root)
pages/*.html      One file per scenario (kebab-case name)
README.md         Public overview + scenario list by category
```

Run locally: open `index.html`, or `python3 -m http.server 8000` (preferred; `file://` breaks some features such as clipboard and auth popups).

## Page conventions

Every scenario page follows the same skeleton (copy `pages/checkboxes.html` as a template):

- `<title>{Name} - Automation Practice Ground</title>`
- Google Fonts links, then `<link rel="stylesheet" href="../styles.css">`
- `.page-wrapper` > `header.header` (logo link + `← Back to list` link to `../index.html`) > `main.main-content > .container` > `footer.footer`
- Content: `h1.page-title`, `p.page-description`, then one or more `.content-card` blocks. Usually ends with a "Testing Tips" card.
- Footer text: `Automation Practice Ground • © 2026 <a href="https://sociabuzz.com/farizagati">Fariz Agati</a>`
- JavaScript is inline in a `<script>` at the end of `<body>`. No shared JS file.
- Reuse classes from `styles.css` (`btn`, `btn-primary`, `form-input`, `flex`, `gap-md`, `mb-lg`, `mt-md`, etc.) and CSS variables (`--color-*`, `--space-*`, `--radius-*`) instead of new CSS or hardcoded values. Add new shared styles to `styles.css` under a sectioned comment header (`/* ==== */`).

## Automation-friendliness rules

- Give every interactive or asserted element a stable, descriptive `id` (e.g. `checkbox-1`, `shadow-button`). Index links use `link-*` ids.
- Intentionally unstable elements (dynamic ids, shifting content, delays, random content) are the point of certain pages. Keep the instability limited to the scenario that advertises it.
- Known credentials in code: form auth `tomsmith` / `SuperSecretPassword!`; basic auth `admin` / `admin` (shown on the index link text).
- Page-specific mechanics worth preserving: Shadow DOM (open root on `#shadow-host`), iframes/nested frames, `window.open` for multiple windows, native `alert/confirm/prompt` for JS alerts.

## Adding a scenario

1. Create `pages/<kebab-name>.html` from the template above.
2. Add a `li.scenario-item > a.scenario-link#link-<name>` entry to `index.html`, in alphabetical order.
3. Add it to the matching category in `README.md`.
4. Update the "40+" count in `index.html` meta description and `README.md` only if it stops being true.

`pages/new-window.html` is a child page opened by Multiple Windows and is intentionally not listed in the index.

## Locator Playground

`locator-playground/` is a separate mini-site (own `index.html` and `styles.css`) built from `docs/XPath Practice Ground MVP Spec.md`. It is exempt from the page skeleton, footer text, Testing Tips and `id` conventions above. Its markup is frozen: copy it from the spec exactly, add no elements or attributes (no `data-testid`), and no teaching text, answers or XPath examples.

## Style

- HTML indentation: 4 spaces in `pages/`, 2 in `index.html`. Match the file you edit.
- Match surrounding code: naming, comment density, idiom. Keep changes minimal and scoped.
- Dark theme with indigo/cyan accents via the existing tokens. Do not introduce a new palette.

## Git

- Default branch: `master`. Work on feature branches (`feat/...`).
- Conventional commit messages.
- Never add AI attribution (no `Co-Authored-By`, no "Generated with" lines) in commits, PRs, code, comments, or docs.

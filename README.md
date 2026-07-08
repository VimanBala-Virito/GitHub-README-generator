# readme.sh — GitHub Profile README Generator

A single-file, terminal-themed web app that generates a polished GitHub profile `README.md` in real time. No frameworks, no build step, no backend — just HTML, CSS, and JavaScript.

![no dependencies](https://img.shields.io/badge/dependencies-none-4dff9f?style=flat-square)
![vanilla](https://img.shields.io/badge/stack-HTML%20%2F%20CSS%20%2F%20JS-4dff9f?style=flat-square)
![license](https://img.shields.io/badge/license-MIT-4dff9f?style=flat-square)

## Preview

A CRT-terminal interface: fill in fields on the left, watch a fully-formed GitHub profile README compile itself on the right, in both raw markdown and rendered preview form.

## Features

- **Live markdown generation** — every keystroke rebuilds the output instantly
- **Identity & bio fields** — name, title, tagline, username, currently working on / learning, fun facts
- **Tech stack chips** — type a language or tool and press Enter to add a shields.io badge
- **Widget toggles** — GitHub stats card, streak stats, top languages, trophies, visitor counter, contribution snake animation
- **Theme picker** — radical, dark, tokyonight, dracula, synthwave, gruvbox (applied across all stat widgets)
- **Animated header options** — typing SVG banner and wave capsule header
- **Socials** — LinkedIn, Twitter/X, personal site, email, Dev.to, Medium, auto-converted to badges
- **Two output views** — raw markdown source and a rendered GitHub-style preview
- **Copy to clipboard** or **download `README.md`** with one click
- **100% client-side** — no data ever leaves your browser

## Usage

1. Download `readme-generator.html`.
2. Open it in any modern browser (double-click, or `open readme-generator.html`).
3. Fill in your details in the left-hand panel — the output updates live.
4. Toggle the widgets and pick a stats theme.
5. Switch to the **preview** tab to see how it'll render on GitHub.
6. Click **copy** or **download README.md**, then drop the file into the special repository named after your GitHub username (e.g. `github.com/yourusername/yourusername`).

No installation, no npm, no server required.

## How it works

The app is a single HTML file:

- **CSS** drives the terminal/CRT aesthetic — scanline overlay, phosphor-green palette, monospace type, animated cursor and scanning header line.
- **JavaScript** reads form input on every change, assembles a markdown string (headers, badges, HTML `<img>`/`<p>` blocks for alignment, and links), and writes it into the output pane.
- A small custom parser turns the generated markdown into rendered HTML for the **preview** tab — no external markdown library is used.
- Stat widgets are generated as image URLs pointing to public services ([shields.io](https://shields.io), [github-readme-stats](https://github.com/anuraghazra/github-readme-stats), [github-readme-streak-stats](https://github.com/DenverCoder1/github-readme-streak-stats), [github-profile-trophy](https://github.com/ryo-ma/github-profile-trophy), [readme-typing-svg](https://github.com/DenverCoder1/readme-typing-svg), [capsule-render](https://github.com/kyechan99/capsule-render)) — these render live once the README is published on GitHub.

## Project structure

```
readme-generator.html   # everything: markup, styles, and logic in one file
```

## Notes

- The **contribution snake animation** requires setting up the [platane/snk](https://github.com/Platane/snk) GitHub Action on your profile repo — the generator inserts the correct `<picture>` tag but the action itself has to be added separately.
- Badge icons for the tech stack use [Simple Icons](https://simpleicons.org/) slugs via shields.io; most common languages and tools resolve automatically.

## License

MIT — use it, fork it, theme it however you like.

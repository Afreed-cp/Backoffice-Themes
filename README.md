![Backoffice Theme Bundle](https://raw.githubusercontent.com/Afreed-cp/Backoffice-Themes/refs/heads/main/assests/logos/logo-white.png)

# Backoffice Theme Bundle

Extra themes for the Umbraco backoffice — including **Christmas** (theme + snow, lights, tree, Santa hat) and popular editor-style themes.

---

## Themes included

| Theme | Style |
|-------|--------|
| **Christmas** | Festive dark palette + effects (snow, lights, tree, Santa) when selected |
| **Neon** | Synthwave / outrun – cyan & magenta on dark |
| **Cyberpunk** | High-contrast pink & blue, chrome accents |
| **Dracula** | Popular dark – purple background, candy accents |
| **Monokai** | Classic high-contrast dark, charcoal + bright accents |
| **VS Blue** | Visual Studio–style light with blue accent |
| **VS Cool Breeze** | VS built-in – light with soft blue tint |
| **VS Icy Mint** | VS built-in – light with mint green tint |

---

## Theme previews

| | | |
|:---:|:---:|:---:|
| **Christmas** | **Neon** | **Cyberpunk** |
| ![Christmas](https://raw.githubusercontent.com/Afreed-cp/Backoffice-Themes/refs/heads/main/assests/themes/Christmas.png) | ![Neon](https://raw.githubusercontent.com/Afreed-cp/Backoffice-Themes/refs/heads/main/assests/themes/Neon.png) | ![Cyberpunk](https://raw.githubusercontent.com/Afreed-cp/Backoffice-Themes/refs/heads/main/assests/themes/Cyberpunk.png) |
| **Dracula** | **Monokai** | **VS Blue** |
| ![Dracula](https://raw.githubusercontent.com/Afreed-cp/Backoffice-Themes/refs/heads/main/assests/themes/Dracula.png) | ![Monokai](https://raw.githubusercontent.com/Afreed-cp/Backoffice-Themes/refs/heads/main/assests/themes/Monokai.png) | ![VS Blue](https://raw.githubusercontent.com/Afreed-cp/Backoffice-Themes/refs/heads/main/assests/themes/VSBlue.png) |
| **VS Cool Breeze** | **VS Icy Mint** | |
| ![VS Cool Breeze](https://raw.githubusercontent.com/Afreed-cp/Backoffice-Themes/refs/heads/main/assests/themes/VSCoolBreeze.png) | ![VS Icy Mint](https://raw.githubusercontent.com/Afreed-cp/Backoffice-Themes/refs/heads/main/assests/themes/VSIcyMint.png) | |

---

## Install

1. **Build the bundle**
   ```bash
   cd templates/ThemeBundle && npm install && npm run build
   ```
2. **Copy to your site** (`App_Plugins/ThemeBundle/`):
   - `dist/umbraco-extension.js` and `dist/effects.entrypoint-*.js`
   - `public/umbraco-package.json`
   - All `public/*.theme.css` and `public/santahatlogo.svg`
3. Restart the application or reload the backoffice. Themes appear in the theme picker; selecting **Christmas** enables the festive effects.

---

## Add more themes

1. Add a new `.theme.css` in `public/` using the same UUI variables as the existing themes (see `dark.theme.css` or any file in this bundle).
2. Register it in `src/bundle.manifests.ts` with `type: "theme"`, a unique `alias`, `name`, and `css` path.
3. Rebuild and redeploy.

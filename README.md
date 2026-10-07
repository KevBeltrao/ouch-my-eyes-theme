# Ouch My Eyes

## Description

Dark theme focused on high contrast. It's available for VSCode (and VSCode-based editors such as Cursor) and Zed, in two variants: **classic blue** and **gray**.

## Installation

### VSCode

Install it [here](https://marketplace.visualstudio.com/items?itemName=KevinBeltrao.kevbeltrao-ouch-my-eyes) or search for "Ouch My Eyes" on VSCode's extension tab.

### Zed

Open the extensions page (`zed: extensions` on the command palette), search for "Ouch My Eyes" and install it. Then pick "Ouch My Eyes (Classic Blue)" or "Ouch My Eyes (Gray)" with `theme selector: toggle`.

### Editor differences

Each editor highlights code in its own way and allows different levels of customization, so a few tokens may look slightly different between VSCode and Zed (e.g. CSS tag selectors or some built-in functions).

## Palette

The primary colors the extension currently uses are:

| Color Name | Color |
|------------|-------|
| Magenta    | ![#ff7df1](https://placehold.co/16x16/ff7df1/ff7df1) #ff7df1 |
| Cyan       | ![#00f3ff](https://placehold.co/16x16/00f3ff/00f3ff) #00f3ff |
| Green      | ![#38ff00](https://placehold.co/16x16/38ff00/38ff00) #38ff00 |
| Yellow     | ![#ffee63](https://placehold.co/16x16/ffee63/ffee63) #ffee63 |
| Gray       | ![#a9b2c2](https://placehold.co/16x16/a9b2c2/a9b2c2) #a9b2c2 |
| Background | ![#0e0f24](https://placehold.co/16x16/0e0f24/0e0f24) #0e0f24 |

The theme might suffer subtle changes as it was just created.

## Examples
Example of the theme using TypeScript
![image](https://github.com/KevBeltrao/ouch-my-eyes-theme/assets/43002117/1ff91a98-361a-4112-955f-0afe6dc269da)

Example using Golang
![image](https://github.com/KevBeltrao/ouch-my-eyes-theme/assets/43002117/049d2396-6dd0-4990-8fc4-f8898e98180d)

## Development

### Project structure

- `themes/`: VSCode themes (`ouch my eyes-color-theme.json` is classic blue, `ouch my eyes-color-darker-theme.json` is gray).
- `zed/`: Zed extension. Both variants live in `zed/themes/ouch-my-eyes.json`.

### Testing locally

- **VSCode:** open this repository and press `F5`. A new window opens with the extension loaded, so you can select the theme there.
- **Zed:** run `zed: install dev extension` from the command palette and select the `zed/` folder. After editing the theme, click "Rebuild" on the dev extension in the extensions page. To check which highlight a token gets, place the cursor on it and run `dev: open highlights tree view`.

### Keeping both editors in sync

The Zed theme was initially generated from the VSCode themes with Zed's [theme importer](https://github.com/zed-industries/zed/tree/main/crates/theme_importer) and then adjusted by hand. Don't regenerate it, or the manual adjustments will be lost. When changing a color, update both `themes/` and `zed/themes/ouch-my-eyes.json`.

### Publishing

- **VSCode:** `yarn ship` (requires `VSCE_TOKEN`).
- **Zed:** bump `version` in `zed/extension.toml`, push, then open a PR to [zed-industries/extensions](https://github.com/zed-industries/extensions) updating the submodule and the version in `extensions.toml`.


**Enjoy!**

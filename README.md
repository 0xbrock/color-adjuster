# Color Adjuster

A simple web tool to lighten or darken colors using HSL color space adjustments (similar to SCSS `lighten()` and `darken()` functions).

## Features

- **Lighten/Darken colors** by a specified percentage
- **Multiple input formats**: `#rgb`, `#rrggbb`, `rgb()`, `rgba()`
- **Visual color picker** for easy color selection
- **Copy to clipboard** - click any color value to copy
- **Side-by-side comparison** of original and adjusted colors
- **Outputs both hex and rgba** formats

## Usage

1. Enter a color in hex (`#3498db`) or rgba (`rgba(52, 152, 219, 1)`) format
2. Set the adjustment percentage (0-100%)
3. Click **Lighten** or **Darken**
4. Click any color value to copy it to your clipboard

## Live Demo

Visit: `https://<username>.github.io/color-adjuster`

## GitHub Pages Setup

1. Push this repository to GitHub
2. Go to **Settings** → **Pages**
3. Under "Source", select **Deploy from a branch**
4. Select the **main** branch and **/ (root)** folder
5. Click **Save**

Your site will be available at `https://<username>.github.io/color-adjuster` within a few minutes.

## Local Development

Simply open `index.html` in a browser. No build step or server required.

## How It Works

Colors are converted to HSL (Hue, Saturation, Lightness) space, the lightness value is adjusted by the specified percentage, then converted back to RGB. This matches the behavior of SCSS color functions.

## License

MIT

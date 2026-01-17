# Color Tool

A web tool for color adjustment and accessibility testing. Lighten/darken colors using HSL adjustments and check WCAG contrast ratios for accessibility compliance.

## Features

### Color Lighten/Darken
- **Adjust lightness** by a specified percentage (like SCSS `lighten()` and `darken()`)
- **Multiple input formats**: `#rgb`, `#rrggbb`, `rgb()`, `rgba()`
- **Visual color picker** for easy color selection
- **Copy to clipboard** - click any color value to copy
- **Side-by-side comparison** of original and adjusted colors
- **Outputs both hex and rgba** formats

### Contrast Checker
- **WCAG contrast ratio** calculation using the official luminance formula
- **AA and AAA compliance** indicators for both normal and large text
- **Live text preview** showing how colors appear at different sizes
- **Swap colors** button to quickly test inverse combinations
- **Text examples** at 24px, 18px, 16px, 14px, and 12px with individual pass/fail badges

## Usage

### Lighten/Darken Colors
1. Enter a color in hex (`#3498db`) or rgba (`rgba(52, 152, 219, 1)`) format
2. Set the adjustment percentage (0-100%)
3. Click **Lighten** or **Darken**
4. Click any color value to copy it to your clipboard

### Check Contrast
1. Enter a text color and background color
2. View the contrast ratio and WCAG compliance levels
3. Use the **Swap Colors** button to test the inverse
4. Review the text examples to see how your colors perform at different sizes

## WCAG Guidelines

| Level | Normal Text | Large Text |
|-------|-------------|------------|
| AA    | 4.5:1       | 3:1        |
| AAA   | 7:1         | 4.5:1      |

**Large text** is defined as 18pt (24px) or 14pt (18.5px) bold.

## Live Demo

Visit: `https://0xbrock.github.io/color-adjuster`

## GitHub Pages Setup

1. Push this repository to GitHub
2. Go to **Settings** → **Pages**
3. Under "Source", select **Deploy from a branch**
4. Select the **main** branch and **/ (root)** folder
5. Click **Save**

Your site will be available at `https://0xbrock.github.io/color-adjuster` within a few minutes.

## Local Development

Simply open `index.html` in a browser. No build step or server required.

## How It Works

### Color Adjustment
Colors are converted to HSL (Hue, Saturation, Lightness) space, the lightness value is adjusted by the specified percentage, then converted back to RGB. This matches the behavior of SCSS color functions.

### Contrast Calculation
Contrast ratios are calculated using the WCAG 2.1 relative luminance formula:
1. Convert RGB values to linear RGB (gamma correction)
2. Calculate relative luminance: `L = 0.2126 * R + 0.7152 * G + 0.0722 * B`
3. Compute contrast ratio: `(L1 + 0.05) / (L2 + 0.05)` where L1 is the lighter color

## License

MIT

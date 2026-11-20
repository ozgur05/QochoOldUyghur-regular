# Qocho Old Uyghur Regular (`v1.000`)

**Qocho Old Uyghur Regular** is an OpenType typeface for the [Old Uyghur script](https://en.wikipedia.org/wiki/Old_Uyghur_script) covering the Unicode [Old Uyghur block (`U+10F70–U+10FAF`)](https://www.unicode.org/Public/17.0.0/charts/PDF/U10F70.pdf) and Manichaean punctuation (`U+10AF2`, Double Dot Within Dot).

The typeface is a glyph-by-glyph geometric reconstruction synthesized from two reference sources—**Noto Serif Old Uyghur** (`95 u` baseline ribbon, scaled by `17/19 ≈ 0.8947`) and **Uigurica Regular** (`75 u` baseline ribbon, scaled by `17/15 ≈ 1.1333`)—normalized to a unified `85.00 u` baseline ribbon with `0.00%` aspect distortion while following the contextual joining and OpenType shaping model documented in [Unicode proposal L2/20-191](https://www.unicode.org/L2/L2020/20191-old-uyghur.pdf).

## Repository Contents

| File / Folder | Description |
| :--- | :--- |
| `QochoOldUyghur-Regular-v1.000.ttf` | Compiled TrueType OpenType font (`v1.000`) ready for desktop and web use |
| `QochoOldUyghur-Regular-v1.000.otf` | Compiled CFF OpenType font (`v1.000`) |
| `QochoOldUyghur-Regular-v1.000-UFO/` | Unpacked Unified Font Object (UFO) master source directory |
| `QochoOldUyghur-Regular-v1.000-UFO.zip` | Compressed archive of the UFO master source |
| `QochoOldUyghurv1.000HarfBuzzTestResult.pdf` | 5-page native HarfBuzz 6.0.0 shaping verification report and 109-glyph specimen |

## Technical Specifications

| Property | Value |
| :--- | :--- |
| **Version** | `1.000` (`109/109` glyphs finalized) |
| **Glyph Inventory** | `103` non-empty outlines + `6` zero-contour format/control slots (`space`, `uni00A0`, `uni200C`, `NULL`, `CR`, `uni200D`) |
| **Unicode Coverage** | Old Uyghur (`U+10F70–U+10FAF`) + Manichaean Double Dot Within Dot (`U+10AF2`) |
| **Units per Em (UPM)** | `1000` |
| **Vertical Metrics** | `Ascender = 1069`, `Descender = -313`, `CapHeight = 617`, `xHeight = 235` |
| **Baseline Ribbon (`T_base`)** | `85.00 u` |
| **GSUB Features** | `aalt`, `ccmp`, `dlig`, `fina`, `init`, `medi`, `rclt`, `rlig`, `salt` |
| **GPOS Features** | `dist` |
| **GDEF Table** | Present |

## Shaping Verification (HarfBuzz 6.0.0)

`QochoOldUyghur-Regular-v1.000.ttf` was tested in native **HarfBuzz 6.0.0** (`RTL`, script tag `Ougr`) across 24 shaping test cases covering positional joining (`init`, `medi`, `fina`), mandatory and discretionary ligatures (`kaph + lesh`, `kaph + waw`, `pe + lesh`, `pe + waw`), combining diacritics, and punctuation:

- **Fallback Check:** `24/24` test cases shaped with zero `.notdef` fallbacks.
- **Reference Parity:** `22/24` exact glyph-name sequence parity against `NotoSerifOldUyghur-fixed.ttf`.
- **Known OpenType Note (`T21` & `T23`):** For `gimelHeth` (`U+10F72`) followed by `twodotsabove` (`U+10F84`), the current `ccmp` lookup substitutes the precomposed `gimelHethtwodotsaboveuyg` glyph, whereas Noto Serif Old Uyghur retains positional `gimelHethuyg.init`/`.medi` with a separate `twodotsaboveuyg` mark. Full details and rendered comparison strips are included in `QochoOldUyghurv1.000HarfBuzzTestResult.pdf`.

## Installation & Usage

1. Download `QochoOldUyghur-Regular-v1.000.ttf` (recommended for general use) or `QochoOldUyghur-Regular-v1.000.otf`.
2. Install the font through your operating system's font manager (Windows Fonts, macOS Font Book, or `~/.local/share/fonts` on Linux).
3. Use an OpenType- and HarfBuzz-compatible application (such as LibreOffice, Chrome/Firefox, XeLaTeX/LuaLaTeX, or modern text editors) with Unicode Old Uyghur text (`U+10F70–U+10FAF`).

## License

[Add your chosen license here, e.g., SIL Open Font License 1.1 (OFL-1.1)]

# Typora Academic Themes

A collection of clean, modern, and high-quality Typora themes designed specifically for scientific writing, seamless LaTeX integration, and elegant code blocks.

## Themes Included

### 1. Academia Light
A LaTeX-inspired minimalist theme that mimics the style of academic papers. 
- **Typography:** Serif fonts (`Source Serif 4`, `Noto Serif SC`) optimized for printing and PDF generation.
- **Tables:** Booktabs-style (LaTeX three-line tables).
- **Vibe:** Serious, clean, academic paper feel.

![Academia Preview](assets/academic.PNG)

### 2. Clarity
A modern, light theme with an elevated card style for code blocks and vibrant syntax highlighting.
- **Typography:** Sans-serif fonts (`Inter`, `Noto Sans SC`) optimized for comfortable on-screen reading.
- **Code Blocks:** Light elevated-card style with vibrant, highly readable syntax highlighting.
- **Vibe:** Modern IDE, clean interface, highly legible.

![Clarity Preview](assets/clarity.PNG)

### 3. Quantum Dark
A deep space / neon dark mode variant optimized for low-light coding and OLED screens.
- **Typography:** Sans-serif fonts paired with JetBrains Mono.
- **Syntax Highlighting:** High-contrast neon accents on a deep `#1e1e2e` background.
- **Vibe:** Geeky, hacker, extremely easy on the eyes in the dark.

![Quantum Dark Preview](assets/quantum-dark.PNG)

### 4. Manuscript
An academic retro style imitating theoretical physics manuscripts.
- **Typography:** Pure serif aesthetic (`Alegreya`, `Palatino Linotype`) for an old-school book feel.
- **Colors:** Solarized Light / Sepia toned background (`#fdf6e3`) with deep brown ink text.
- **Vibe:** Immersive, retro, reading a decades-old physics manuscript.

![Manuscript Preview](assets/manuscript.PNG)

### 5. Vitae (Academic CV)
A distinctive résumé/CV theme that combines scholarly gravitas with modern editorial design.
- **Typography:** Elegant serif headings (`Cormorant Garamond`) paired with clean sans-serif body (`Inter`). Skills render as teal pill badges.
- **Layout:** Compact line spacing (1.4–1.5) optimized for dense CV content and A4 PDF export.
- **Signature:** Gradient accent rule under the name, teal-accented section dividers, and editorial-quality heading hierarchy (H1=Name, H2=Sections, H3=Institutions, H4=Positions, H5=Dates).
- **Vibe:** Stands out instantly among hundreds of LaTeX-default CVs while maintaining academic professionalism.

## Installation

The easiest way to install these themes is via Typora's built-in theme folder access.

### Method 1: Via Typora (Recommended)

1. Open **Typora**.
2. Open **Preferences** (Settings):
   - **macOS**: `Typora` -> `Settings` (or `Cmd + ,`).
   - **Windows/Linux**: `File` -> `Preferences` (or `Ctrl + ,`).
3. Navigate to the **Appearance** tab.
4. Click the **Open Theme Folder** button.
5. Copy all `.css` files (and any optional asset folders) from this repository into the opened folder.
6. **Restart Typora**.
7. Select your preferred theme from the `Themes` menu in the top bar.

### Method 2: Manual Path

If you prefer to navigate directly, the default theme paths are:

- **Windows**: `%AppData%\Roaming\Typora\themes\`
- **macOS**: `~/Library/Application Support/abnerworks.Typora/themes/`
- **Linux**: `~/.config/Typora/themes/`

Simply paste the `.css` files into the corresponding directory and restart the application.

## Features

- **Cross-Platform Compatibility**: Uses Google Fonts accompanied by optimal fallback system fonts for Windows, macOS, and Linux. No font installation required.
- **LaTeX Math Support**: Perfectly integrated math formatting for both inline `$ ... $` and block `$$ ... $$` math.
- **PDF Export Setup**: Automatically formatted for professional print / PDF layouts.
- **Academic Tables**: Clean, minimalist table styling (Booktabs) focusing on data readability.

## Testing Your Theme

You can open the `academia_preview.md` file included in this repository to test how the various elements (Math, Code, Tables, Blockquotes, Lists) render in your selected theme.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

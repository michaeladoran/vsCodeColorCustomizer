# VS Code Theme Customizer

A single-file web app for customizing your VS Code colors. Tweak workbench and syntax
colors against a live VS Code mockup, then copy the generated JSON into your settings.

## How to run

Just open [index.html](index.html) in any browser — no install, no build step.
(Double-click the file, or drag it into a browser window.)

## How to use

1. **Pick colors** in the left panel. Everything starts at VS Code's Dark+ defaults.
   The panel has three tabs:
   - **Interface** — the UI chrome (Editor, Title Bar, Activity Bar, Side Bar, Tabs,
     Status Bar, Panel) via `workbench.colorCustomizations`. Sections expand one at a
     time; the little dots on each header show that section's current colors at a glance.
   - **Code** — syntax highlighting (comments, strings, keywords, functions…) via
     `editor.tokenColorCustomizations` textMate rules, each with **B**old / *I*talic toggles.
   - **Presets** — save and load named themes.
2. **Click any color chip** to open the built-in picker: drag in the shade square, slide
   the hue bar, type a hex value, reuse a recent color, or grab any on-screen color with
   the eyedropper (Chrome/Edge). Close it by clicking anywhere else or pressing Esc.
3. Watch the **preview** update live as you change values.
4. Click **Copy JSON**, then in VS Code press `Ctrl+Shift+P` →
   *Preferences: Open User Settings (JSON)* and paste the keys in.
   By default only colors you changed are included; check *Include unchanged colors*
   to export everything.

## Extras

- **Import JSON** — paste your existing settings.json (comments and trailing commas are fine)
  to load your current customizations and keep tweaking.
- **Presets** — save named themes to browser localStorage and reload them later.
- **🎲 Randomize** — generates a harmonious random palette as a starting point.
- **↺ Reset to Dark+** — back to the defaults.
- Your work-in-progress is autosaved to localStorage, so a refresh won't lose it.

## Notes

- The generated customizations apply on top of whatever theme you're using. They aren't
  scoped to a specific theme; to scope them, wrap the workbench colors in a
  `"[Theme Name]": { … }` block yourself.
- Colors are plain 6-digit hex. VS Code also accepts 8-digit hex with alpha if you want
  to hand-edit transparency afterwards.

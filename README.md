# Mumble UI Overhaul (Windows 11-aligned)

This repository now targets Mumble's real desktop stack (Qt on Windows) with a **Windows 11-inspired** styling baseline.

## What changed
- Replaced the earlier minimal baseline with a broader, Fluent-inspired stylesheet: `mumble-minimal.qss`.
- Expanded coverage to include menus, bars, grouped panels, primary/secondary buttons, text inputs, list/table/tree selections, tabs, scrollbars, and tooltip surfaces.

## Important limitation (so expectations are correct)
Qt stylesheets can style widget visuals, but they **cannot fully replicate WinUI/Windows App SDK internals** such as:
- Mica/acrylic materials
- Composition animations
- Native WinUI control templates
- Dynamic system theme/accent plumbing without app-side code

So this repository provides the strongest possible QSS-based approximation.

## How to test in Mumble on Windows
1. Copy `mumble-minimal.qss` to your Windows machine.
2. Open Mumble.
3. Go to settings/preferences and locate stylesheet or style override.
4. Select this `.qss` file.
5. Restart Mumble if needed.

## Manual validation checklist
- Menus and app bars look flat/clean with light separators.
- Primary actions appear as blue Fluent-style buttons.
- Inputs have 8px rounded corners and blue focus borders.
- Tables/lists/trees show soft selected-row highlight.
- Tabs and scrollbars have modern rounded styling.

## Optional app-code hooks for deeper overhaul
If you can modify Mumble source, add object/dynamic properties to enable richer patterns. Example:
- `QPushButton[variant="secondary"]` for tertiary button types (already included in QSS)
- Semantic classes/object names for nav panes, command bars, and section headers

Then map those selectors in QSS for a more complete Windows 11 information hierarchy.

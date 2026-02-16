# Mumble Custom UI (Windows)

This repository now targets **Mumble's actual desktop UI stack** (Qt on Windows), not browser HTML/CSS.

## Why this changed
Mumble is a native Windows desktop app, so standalone `index.html`/`styles.css` files do not control the Mumble client UI.
A Qt stylesheet (`.qss`) is a more realistic baseline for visual customization.

## Included file
- `mumble-minimal.qss`: Minimal black-and-white theme baseline with readable contrast, clean borders, and simple modern controls.

## How to test this in Mumble (Windows)
1. Save `mumble-minimal.qss` somewhere on your Windows machine (for example: `C:\Users\<you>\Documents\mumble-minimal.qss`).
2. Open Mumble.
3. Go to Mumble settings/preferences and find the **stylesheet / Qt style override** option (location may differ by Mumble version).
4. Point Mumble to this `.qss` file.
5. Restart Mumble if required.

## Validation checklist
- Main window, menus, and dialogs are white with dark text.
- Buttons are black with white text, with sensible disabled styling.
- Text inputs and lists use subtle gray borders.
- Focused controls have a clearer dark border.

## Notes
- Not all Mumble widgets are guaranteed to expose style hooks identically across versions.
- If specific controls remain unchanged, inspect their Qt class names and add targeted selectors.

# Windows 11 UI Overhaul Plan for Mumble

This plan describes what is needed for a **full** overhaul beyond stylesheet-only adjustments.

## 1) Visual language baseline
- Typography: Segoe UI Variable Text (fallback to Segoe UI)
- Radius system: 8px standard controls, 12px larger surfaces
- Spacing scale: 4 / 8 / 12 / 16 / 24 px
- Color roles: canvas, surface, stroke, text primary/secondary, accent, focus

## 2) Navigation architecture
- Move major views into a left navigation rail with clear section grouping
- Keep top-level command actions in a command bar
- Ensure persistent context indicators (active server/channel)

## 3) Density and hierarchy
- Define compact/comfortable density modes
- Raise visual contrast between:
  - active vs inactive channel rows
  - read vs unread status elements
  - destructive vs neutral actions

## 4) Input and feedback patterns
- Standardize focus visuals (accent stroke + predictable tab order)
- Standardize disabled semantics and visual style
- Add non-blocking inline validation for forms/settings

## 5) Accessibility expectations
- Keyboard-only navigation parity
- Screen reader label audit for all interactive controls
- Contrast targets aligned with WCAG AA (text and non-text controls)

## 6) Technical execution path
1. Introduce semantic object names/properties in UI code.
2. Split QSS by concerns (base, controls, navigation, data views).
3. Add screenshots for key screens (home/server/channel/settings).
4. Add regression checklist for every release.

## 7) Definition of done
- No legacy-looking controls in primary flows
- Consistent radii, spacing, and focus affordances across views
- Usability pass completed for mouse + keyboard + screen reader users

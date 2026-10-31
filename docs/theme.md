# Theme Toggle

The calculator ships with a light and a dark theme, switched from the
toggle in the app header.

## How it works

- The app starts in the **light** theme.
- Pressing the toggle flips between `light` and `dark` and writes the
  choice to the `data-theme` attribute on the document root, so every
  component restyles from the same switch.
- The toggle lives in its own component (`ThemeToggle`), separate from
  the calculator itself, so the theme logic stays out of the calculation
  code.

## Notes

- The theme only affects styling — it never touches the current
  expression, the result, or the history.
- Switching mid-calculation is safe: the expression on screen is
  untouched.

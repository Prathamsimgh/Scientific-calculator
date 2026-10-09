# Project Structure

## Layout

```
src/
  main.jsx                 # vite entry point
  App.jsx                  # theme state, renders theme toggle + calculator
  App.css / index.css      # styles
  assets/
  components/
    Calculator.jsx         # the calculator itself
    ThemeToggle.jsx        # light/dark toggle button
    Icons.jsx              # button icons
index.html                 # html shell
vite.config.js             # vite config
eslint.config.js           # lint config
```

## How it fits together

- `App.jsx` owns the theme (`light` / `dark`). Toggling writes the value to
  `document.documentElement`'s `data-theme` attribute so CSS picks it up.
- `Calculator.jsx` owns all calculator state:
  - `display` — current expression/result string.
  - `memory` — memory register (MC, M+, M-, MR).
  - `isRad` — radians vs degrees for trig.
  - `secondFunction` — shift-style secondary keys.
  - `history` — list of past `expression = result` entries.
  - open-parentheses tracking — equals auto-closes any unclosed `(` before
    evaluating.
- Expressions are evaluated with **mathjs** (`math.evaluate`); failures show
  `Error`.
- A successful evaluation records the entry in history and plays a confetti
  animation (`react-confetti-explosion`) for ~3s.

## Running it

```
npm install
npm run dev
```

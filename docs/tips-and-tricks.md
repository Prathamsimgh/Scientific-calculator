# Tips & Tricks

Little things the calculator does that aren't obvious from the buttons.

## Building an expression

Type the whole expression first, then hit `=` — `2 + 3 × 4` evaluates with
normal operator precedence (mathjs), not left-to-right.

## Parentheses auto-close

Open as many `(` as you want — you don't have to close them. `=` closes all
open parentheses for you before evaluating. Pressing `)` is only needed when
you want to close them explicitly mid-expression.

## Powers and roots

- `xʸ` appends a `^`: press `2`, `xʸ`, `1`, `0`, `=` → `2^10` = 1024.
- `ʸ√x` works in reverse order: enter the number **first**, then the key,
  then the root degree. `27`, `ʸ√x`, `3`, `=` → 3.

## Sign, percent, and notation

- `±` flips the sign of the current value (`-Number(display)`).
- `%` divides the current value by 100.
- `EE` appends `e` for scientific notation: `5`, `EE`, `6` → `5e6` (five
  million).

## Rad / Deg and 2ⁿᵈ

- The `Rad`/`Deg` button toggles how `sin`/`cos`/`tan` interpret the input.
  Default is radians.
- The `2ⁿᵈ` key swaps `sin`/`cos`/`tan` for their hyperbolic versions
  (`sinh`/`cosh`/`tanh`).

## History

Every `=` result is appended to the History panel under the buttons, so you
can scroll back through what you computed. (Also: a successful `=` earns you
a confetti burst.)

## Recovering from a mistake

- `C` clears the display back to `0` and resets any half-built power/root
  input.
- Anything that can't be evaluated (division by zero, `√` of a negative,
  broken expression) shows `Error` on the display — just `C` and retype.

## Memory

- `m+` / `m−` add or subtract the displayed value into memory; `mr` recalls
  it onto the display; `mc` zeroes it.

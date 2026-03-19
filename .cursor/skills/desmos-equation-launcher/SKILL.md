---
name: desmos-equation-launcher
description: Generate URLs for the Desmos Equation Launcher to graph mathematical equations. Use when the user wants to visualize equations, graph functions, or needs a shareable link to render math in Desmos. Handles single or multiple equations with proper URL encoding.
---

# Desmos Equation Launcher

Generate URLs that render equations in an embedded Desmos calculator.

## URL Format

**Base URL:** `https://error9098x.github.io/desmos-launcher/`

**Single equation:**
```
https://error9098x.github.io/desmos-launcher/?eq=y=x^2
```

**Multiple equations:**
```
https://error9098x.github.io/desmos-launcher/?eq1=y=x^2&eq2=y=sin(x)
```

## URL Encoding

Use URL encoding for special characters:

| Character | Encoded |
|-----------|---------|
| `=` | `%3D` |
| `^` | `%5E` |
| `+` | `%2B` |
| Space | `%20` or `+` |

## Examples

**Quadratic function:**
```
?eq=y=x%5E2
```

**Sine wave:**
```
?eq=y=sin(x)
```

**With parameters (creates sliders):**
```
?eq=y=a*sin(bx)
```

**Implicit equation:**
```
?eq=x%5E2%2By%5E2=1
```

**System of equations:**
```
?eq1=y=2x%2B1&eq2=y=-x%2B3
```

## Features

- Automatic slider creation for undefined variables (a, b, c, etc.)
- KaTeX rendering for pretty equation display
- "Open in Desmos" link for full calculator experience
- Dark mode interface
- Mobile-friendly touch interactions

## Behavior

- If no `eq` parameter: shows error state with link to Desmos
- Equations without `=` are auto-prefixed with `y = `
- All URL encoding is handled client-side

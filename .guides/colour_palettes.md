# Colour Palettes

## Colour Roles

| Role | Token | Used for |
|------|-------|----------|
| **Primary** | `--link-color`, `--hover-bg` | Links, nav, profile, timeline, conference labels |
| **Accent** | `--accent-color`, `--accent-hover` | Publication action button hover (Paper, Code, Demo) |
| **Neutral** | `--bg-color`, `--text-color`, `--muted-color`, `--border-color` | All layout and text |

Primary is palette-driven (switchable). Accent (amber) and neutrals are fixed.

---

## Switch the Primary Palette

Change one line in `content/site/config.yaml`:

```yaml
active_palette: "teal"  # Options: indigo | violet | teal
```

Reload in browser — JS reads the palette and applies the brand colour automatically.

---

## Palette Reference

| Name | Light link | Light hover | Dark link | Dark hover |
|------|-----------|-------------|-----------|------------|
| `indigo` | `#4f46e5` | `#e0e7ff` | `#818cf8` | `#2d2a5e` |
| `violet` | `#7c3aed` | `#ede9fe` | `#a78bfa` | `#2e1065` |
| `teal`   | `#0d9488` | `#ccfbf1` | `#2dd4bf` | `#042f2e` |

---

## Accent (Fixed)

Amber — used for publication action button hover. Brightens in dark mode.

| | Base | Hover fill |
|--|------|------------|
| Light | `#f59e0b` | `#fef3c7` |
| Dark | `#fbbf24` | `#451a03` |

---

## Adding a New Palette

Add an entry under `design.colors.palettes` in `content/site/config.yaml`:

```yaml
my-palette:
  light: { link: "#hex", hover: "#hex" }
  dark:  { link: "#hex", hover: "#hex" }
```

Then set `active_palette: "my-palette"`. No CSS changes needed.

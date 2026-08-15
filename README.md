# KGR Cup Countdown

A single standalone page counting down to KGR Cup (Fall '26) opening night —
Saturday, September 5, 2026, 7:00 PM at Gameville, Greenfield District.

Plain HTML + CSS + vanilla JS. No framework, no build step. Open `index.html`
in a browser, or serve the directory with any static file server.

```
python3 -m http.server 8000
```

## Structure

```
index.html                          # nav + hero, inline styles and clock script
app/styles.css                      # KGR design system — shared, do not modify
uploads/pasted-1786796703887-0.png  # hero photo
```

`app/styles.css` is taken verbatim from the KGR design system project and owns
every shared token (`--ink`, `--accent`, `--cream`, …) plus `.kgr-*` components.
Countdown-specific rules are namespaced `.cd-*` and live inline in `index.html`.

## Design notes

The page occupies exactly one viewport and never scrolls. Vertical rhythm is
sized with `vh`-aware `clamp()` so the composition compresses on short screens
instead of overflowing, with a dedicated compact layout for landscape phones.

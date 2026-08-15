# uploads

Drop the hero photo here.

**Expected filename:** `pasted-1786796703887-0.png`

**Source:** Claude Design project `bc4876af-f979-4c5e-b534-f6dd1a5eba66`,
at the path `uploads/pasted-1786796703887-0.png`.

The final path must be, exactly:

```
uploads/pasted-1786796703887-0.png
```

That is what `index.html` references. If you'd rather use a different filename,
update the `src` on `#hero-img` in `index.html` to match.

## If the file is missing

The page still works. The radial veil sits over the page background, so an
absent photo reads as a dim hero rather than a broken image — the script drops
the `<img>` element when the load fails, so no broken-image icon or stray alt
text appears. Nothing else about the layout changes.

## Notes

The image is rendered `object-fit: cover` with `object-position: center 40%`,
under `saturate(.85) contrast(1.05)`, and is heavily darkened by the veil. A
wide landscape photo works best; fine detail will not survive the veil.

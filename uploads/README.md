# uploads

The hero photo.

```
uploads/pasted-1786796703887-0.jpeg
```

720 × 377 progressive JPEG — an aerial view of the KGR residential towers and
the surrounding city, with a KGR logo watermark near the centre. Originally
exported from Claude Design project `bc4876af-f979-4c5e-b534-f6dd1a5eba66`.

That path is what the `src` on `#hero-img` in `index.html` references. Replacing
the photo means updating that `src` and the image's `alt` text to match.

## Resolution

At 720px wide the image is upscaled roughly 2× on a desktop viewport, so it is
visibly soft at full size. The veil hides most of that. A higher-resolution
export would sharpen the hero if one is available.

## If the file is missing

The page still works. The radial veil sits over the page background, so an
absent photo reads as a dim hero rather than a broken image — the script drops
the `<img>` element when the load fails, so no broken-image icon or stray alt
text appears. Nothing else about the layout changes.

## Notes

The image is rendered `object-fit: cover` with `object-position: center 40%`,
under `saturate(.85) contrast(1.05)`, and is heavily darkened by the veil. A
wide landscape photo works best; fine detail will not survive the veil.

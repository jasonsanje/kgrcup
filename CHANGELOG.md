# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/).

## [Unreleased]

### Added
- Countdown hero page (`index.html`): sticky-height mini-nav, full-bleed hero
  photo with radial veil, kicker, display headline, subtitle, live D:H:M:S clock
  with per-digit boxes, Facebook community CTA and a note line.
- Live clock counting to 2026-09-05 19:00 local time, ticking every second. Days
  pad to two digits and keep their natural width above 99; hours, minutes and
  seconds always pad to two. At or past the target every unit shows `00`, the
  clock takes an accent treatment and the note reads "The season is underway".
- Single-viewport layout that never scrolls: `100dvh` flex column, 64px nav,
  `flex: 1` hero. Vertical rhythm uses `vh`-aware `clamp()` so the composition
  compresses rather than overflows, with a dedicated compact layout for
  landscape phones under 430px tall so the CTA is never clipped.
- Accessibility beyond the source design: the digit grid is `aria-hidden`, with
  a visually hidden `aria-live="polite"` region carrying the countdown as a
  sentence built from days, hours and minutes so it updates on the minute rather
  than every second; the digit tick animation is disabled under
  `prefers-reduced-motion: reduce`; the hero image has descriptive alt text.
- `app/styles.css`, the KGR design system stylesheet, taken verbatim.
- Hero photo `uploads/pasted-1786796703887-0.jpeg`, an aerial view of the KGR
  residential towers, with alt text describing it.

### Changed
- Strengthened the hero veil. The source design's gradient was tuned against a
  placeholder; against the real daylight aerial it left the kicker and subtitle
  on sunlit buildings at poor contrast. The radial centre stop goes from 45% to
  66% opacity and a soft vertical scrim sits behind the type.

[Unreleased]: https://github.com/jasonsanje/kgrcup/commits/main

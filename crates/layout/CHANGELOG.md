# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.0](https://github.com/suveshmoza/browser/compare/v0.0.1...v0.2.0) - 2026-07-01

### Added

- *(svg)* SVG IDL conformance — idlharness.window.html to 100% ([#119](https://github.com/suveshmoza/browser/pull/119))
- *(engine)* forced-colors backplate spans the line box (pre-pass)
- *(style)* :visited privacy — keep LinkText computed, map to VisitedText at paint
- *(layout)* nested-flex-wrap baselines — line-aware descent + inline-block cross height
- *(layout)* grid cross-axis align-items (incl. baseline) — grid-001 green
- *(style,layout)* grid-template shorthand + grid flex baseline
- *(style,layout)* table flex baseline, caption-side, dispatch (table-001 green)
- *(style,layout)* multi-column layout (multicol-001 green)
- *(style,layout)* -webkit-line-clamp last baseline from the Nth line (line-clamp-001 green)
- *(layout)* central baseline for parallel vertical flex items (006/007 green)
- *(layout)* writing-mode-aware flex main axis
- *(layout)* orthogonal-flow flex baseline + vertical item cross-sizing (005 green)
- *(style,layout)* logical sizes + scroll-container baseline clamp (overflow-001 green)
- *(layout)* fieldset legend rendering (first green flex-baseline file)
- *(layout)* abspos flex children take their static position from justify-content/align-self
- *(layout)* vertical writing-mode box geometry (stage 1)
- *(style,layout)* resolve em in width/height against the element font-size; flex baseline alignment
- *(css)* clip overflow:hidden content
- *(css)* support box-sizing: border-box
- *(css)* render background-image url() (size/repeat/position)
- *(css)* pass all css/CSS2/positioning via scroll-clamp, text-indent, inline static position, and @font-face web fonts ([#107](https://github.com/suveshmoza/browser/pull/107))
- *(layout)* CSS floats plus Wikipedia rendering and cascade-perf fixes ([#105](https://github.com/suveshmoza/browser/pull/105))
- *(layout,cssom)* resolve percentage width + report used width/height
- *(cssom)* getComputedStyle reports used margins (resolved auto)
- *(layout)* resolve auto margins — `margin: 0 auto` block centering
- *(layout)* block-in-inline — blockify an inline element with block children
- *(cssom)* resolved used insets for positioned boxes + named window globals
- *(style,layout,engine)* CSS mask-image (the icon technique)
- *(style,layout,engine)* border-collapse + HTML presentational table attributes
- *(dom)* img width/height attrs + alt, naturalWidth/Height, dialog API, textarea/select .value
- *(engine,layout)* render inline <svg> (was a 0x0 box, zero graphics)
- *(forms)* render input/progress/meter as real widgets; label hit box
- *(layout,style)* real HTML table layout (was inline cells / vanishing rows)
- *(style,layout,paint)* block-level default rendering (margins, br, pre, hr, list markers)
- *(style,layout,paint)* default styling for inline text elements
- real Canvas 2D context (display list in JS, rasterized + composited by the engine)
- 279 HTML named entities + CSS ::before/::after generated content
- proper caret bar (not '|' glyph) + clickable <select> dropdowns (NSMenu)
- *(layout)* render <select> as a dropdown (selected option + ▾), not inline options
- *(css,style,engine)* linear/radial gradients, box-shadow, transform (translate/scale/rotate)
- checkboxes/radios, change/focus/blur/submit, hover events, text caret
- text form input — typing, value rendering, input/keydown events; fix load race
- *(css)* max/min sizing, line-height, text-transform, text-decoration, opacity, border-radius, logical props
- *(layout,engine,ffi,app)* clickable links (hit-test <a href> -> navigate)
- *(paint,layout,engine)* render <img> images (fetch, decode, blit)
- *(layout)* box-model layout with flexbox, grid, and positioning

### Fixed

- *(layout)* use grid-area containing blocks for abspos grid children ([#115](https://github.com/suveshmoza/browser/pull/115))
- *(layout)* <br> between block siblings creates a line box
- *(layout)* resolve percentage height + fill width:100%/height-constrained tables
- *(layout)* count inline-block atomics in intrinsic width
- *(layout)* exclude table captions from a table's flex baseline
- *(layout)* cross size of vertical-container flex items from laid-out width
- *(layout)* weighted flex-shrink + percentage flex-basis
- *(layout)* resolve explicit/percentage width on inline-blocks
- *(layout)* flow inline-level content beside floats
- *(layout)* textarea renders its text content (was blank, ~4px tall)
- *(style,layout)* defensively skip out-of-bounds child ids in render walkers

### Other

- satisfy rustfmt and clippy (-D warnings)
- run cargo test on PRs (Linux only) ([#86](https://github.com/suveshmoza/browser/pull/86))
- split monolithic lib.rs files into focused modules ([#59](https://github.com/suveshmoza/browser/pull/59))
- format workspace with rustfmt + make clippy clean (enforced in CI)

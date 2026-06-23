# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.1.1](https://github.com/suveshmoza/browser/compare/v0.1.0...v0.1.1) - 2026-06-23

### Added

- *(css)* support box-sizing: border-box
- *(css)* resolve rem against the root font-size
- *(css)* pixel background-position and background-size (CSS sprites)
- *(css)* render background-image url() (size/repeat/position)
- *(css)* pass all css/CSS2/positioning via scroll-clamp, text-indent, inline static position, and @font-face web fonts ([#107](https://github.com/suveshmoza/browser/pull/107))
- *(layout)* CSS floats plus Wikipedia rendering and cascade-perf fixes ([#105](https://github.com/suveshmoza/browser/pull/105))
- *(dom)* implement innerText/outerText getter and setters ([#50](https://github.com/suveshmoza/browser/pull/50))
- *(cssom)* aspect-ratio tracked; resolved min-width/min-height:auto
- *(cssom)* logical longhands in getComputedStyle enumeration + 'all' coverage
- *(cssom)* iframe-document getComputedStyle (per-frame cascade, media + % widths)
- *(cssom)* writing-mode/direction-aware static position for inset resolved values
- *(cssom)* resolve background-image url() against the correct base URL
- *(layout,cssom)* resolve percentage width + report used width/height
- *(layout)* resolve auto margins — `margin: 0 auto` block centering
- *(css,cssom)* namespace selector matching, @property, font-face rules, shorthand/all serialization
- *(cssom)* font-variant/font-family serialization, decl validation, @page/@keyframes restrictions, :lang(), MO style records
- *(cssom)* fix declaration/serialization/rule/MediaList CSSOM tests (css/cssom 3005→3093)
- *(cssom)* CSSStyleDeclaration shorthands + custom properties
- *(cssom)* resolved insets, value serialization, CSSStyleRule.selectorText, !important
- *(style,engine)* implement CSS color-scheme for dark UA defaults
- *(style,layout,engine)* border-collapse + HTML presentational table attributes
- *(theme)* prefers-color-scheme reflects the real macOS appearance
- *(dom)* img width/height attrs + alt, naturalWidth/Height, dialog API, textarea/select .value
- *(forms)* render input/progress/meter as real widgets; label hit box
- *(layout,style)* real HTML table layout (was inline cells / vanishing rows)
- *(style,layout,paint)* block-level default rendering (margins, br, pre, hr, list markers)
- *(style,layout,paint)* default styling for inline text elements
- 279 HTML named entities + CSS ::before/::after generated content
- *(style,js)* real getComputedStyle() backed by the in-Session cascade (was a stub returning '')
- *(css,style,engine)* linear/radial gradients, box-shadow, transform (translate/scale/rotate)
- *(css,style)* full selector engine — combinators, pseudo-classes, attribute selectors
- *(style,engine)* media/container queries + vw/vh use real viewport+DPR (responsive on resize)
- *(css,style)* clamp()/min()/max()/calc() length math + @container queries
- *(css)* max/min sizing, line-height, text-transform, text-decoration, opacity, border-radius, logical props
- *(css,style)* apply @layer rules + parse rgb()/hsl()/oklch()/var(); drop debug bar
- *(css,style)* CSS parser and cascade (box, flex, grid, position props)

### Fixed

- *(layout)* weighted flex-shrink + percentage flex-basis
- *(svg)* parse packed path numbers; prefer url() background layer
- *(style)* getComputedStyle('direction') returns its value, not always 'ltr'
- *(style)* match [*|attr] / [|attr] attribute selectors (namespace prefix)
- *(css,style)* resolve url() against the stylesheet's own URL, not the document
- *(engine,style)* default page canvas to white + black text (was a dark gradient)
- render <details>/<summary> + other block elements; click summary to toggle
- *(style)* parse em/rem in lengths (margin/padding/border-width/width/...) — fixes invisible fieldset card borders
- *(style)* compute percentage font-size (font-size: N% = N% of parent) — fixes browserscore big number
- *(style,layout)* defensively skip out-of-bounds child ids in render walkers

### Other

- run cargo test on PRs (Linux only) ([#86](https://github.com/suveshmoza/browser/pull/86))
- split monolithic lib.rs files into focused modules ([#59](https://github.com/suveshmoza/browser/pull/59))
- format workspace with rustfmt + make clippy clean (enforced in CI)
- Merge commit 'ea635f8'
- Merge commit '30f0f86f8c120e067aca467605bed0d03bb6e4f2'
- Merge branch 'worktree-agent-abdcecdd6c488230d'
- *(style)* index rules by key selector (cascade O(nodes×rules) -> O(nodes×candidates))

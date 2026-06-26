# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.0](https://github.com/suveshmoza/browser/compare/v0.0.22...v0.2.0) - 2026-06-26

### Added

- *(css)* pass all css/CSS2/positioning via scroll-clamp, text-indent, inline static position, and @font-face web fonts ([#107](https://github.com/suveshmoza/browser/pull/107))
- *(css,cssom)* namespace selector matching, @property, font-face rules, shorthand/all serialization
- *(cssom)* CSSStyleDeclaration shorthands + custom properties
- *(css,style)* full selector engine — combinators, pseudo-classes, attribute selectors
- *(css,style)* clamp()/min()/max()/calc() length math + @container queries
- *(css,engine)* follow @import (recursive fetch) + CSS nesting (&)
- *(css,style)* apply @layer rules + parse rgb()/hsl()/oklch()/var(); drop debug bar
- *(css,style)* CSS parser and cascade (box, flex, grid, position props)

### Fixed

- *(css)* unterminated string ends at newline (bad-string recovery); feat(wpt-runner): .sub substitution + .headers
- *(css,style)* resolve url() against the stylesheet's own URL, not the document

### Other

- format workspace with rustfmt + make clippy clean (enforced in CI)

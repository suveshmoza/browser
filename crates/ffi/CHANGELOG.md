# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.0](https://github.com/suveshmoza/browser/compare/v0.1.0...v0.2.0) - 2026-07-02

### Added

- *(engine)* site favicons in the tab and address bar
- *(net)* URL fixup, HSTS, and http fallback in the engine (not the shell)
- tab tooltip shows per-tab CPU + memory usage
- *(theme)* prefers-color-scheme reflects the real macOS appearance
- *(devtools)* Elements DOM inspector tab (tree view + click-to-highlight on page)
- page text selection (drag to select, highlight, ⌘C copy)
- proper caret bar (not '|' glyph) + clickable <select> dropdowns (NSMenu)
- progressive/streaming first paint (Phase 1) — paint HTML as it downloads
- *(net,engine,ffi)* devtools backend — network log + console REPL eval
- mousedown/mouseup/dblclick/contextmenu events (Engine::dispatch_mouse)
- checkboxes/radios, change/focus/blur/submit, hover events, text caret
- live JS event loop — pump timers/animations after load (Engine::tick)
- text form input — typing, value rendering, input/keydown events; fix load race
- interactive pages — persistent per-tab JS runtime + click dispatch
- *(engine,ffi,app)* tab titles from <title>; default homepage browserscore.dev
- *(layout,engine,ffi,app)* clickable links (hit-test <a href> -> navigate)
- *(engine,ffi,app)* mouse-wheel scrolling for page content
- *(ffi)* C ABI with cbindgen-generated header

### Fixed

- *(js,ffi)* validate JS node ids vs arena + catch_unwind render backstop

### Other

- format workspace with rustfmt + make clippy clean (enforced in CI)

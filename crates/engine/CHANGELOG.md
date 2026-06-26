# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.0](https://github.com/suveshmoza/browser/compare/v0.0.0...v0.2.0) - 2026-06-26

### Added

- *(engine)* CSS Custom Highlight API + ::highlight(name) painting
- *(engine)* paint ::selection for programmatic getSelection() highlights
- *(engine)* forced-colors backplate spans the line box (pre-pass)
- *(style)* forced color inherits + SVG/visited currentColor mapping
- *(engine)* render uniform SVG gradients as solid fills
- *(engine)* force non-system SVG gradient stop-colors in forced colors
- SVG fill/stroke currentColor follows the forced color
- background-image viewport propagation + SVG forced-color-adjust:none default
- *(engine)* SVG reads CSS fill/stroke + forces them in forced colors
- *(style)* :visited privacy — keep LinkText computed, map to VisitedText at paint
- *(engine)* viewport background uses only <html> in forced colors
- self.crossOriginIsolated from COOP+COEP response headers
- *(js)* dedicated Web Workers (per-realm) and OffscreenCanvas
- *(engine)* reconstruct WOFF2 glyf/loca/hmtx table transforms
- *(engine)* render @font-face web fonts, including WOFF2 decoding
- *(css)* clip overflow:hidden content
- *(svg)* linear/radial gradient fills
- *(svg)* nested <svg> viewports and <use> references
- *(css)* pixel background-position and background-size (CSS sprites)
- *(engine)* render direct image navigations as images
- *(css)* render background-image url() (size/repeat/position)
- *(engine)* font fallback for non-Latin glyphs
- *(engine)* decode SVG images in img tags
- *(engine)* site favicons in the tab and address bar
- *(net)* URL fixup, HSTS, and http fallback in the engine (not the shell)
- *(css)* pass all css/CSS2/positioning via scroll-clamp, text-indent, inline static position, and @font-face web fonts ([#107](https://github.com/suveshmoza/browser/pull/107))
- *(layout)* CSS floats plus Wikipedia rendering and cascade-perf fixes ([#105](https://github.com/suveshmoza/browser/pull/105))
- *(dom)* CharacterData methods, CDATASection, and arena-backed off-documents ([#3](https://github.com/suveshmoza/browser/pull/3))
- *(engine)* add JPEG XL (.jxl) image decoding ([#4](https://github.com/suveshmoza/browser/pull/4))
- *(engine)* cross-platform system-font discovery (macOS/Linux/Windows)
- *(css)* enforce stylesheet MIME type — non-text/css link responses don't apply
- *(cssom)* getComputedStyle reports used margins (resolved auto)
- tab tooltip shows per-tab CPU + memory usage
- *(js,engine)* real elementFromPoint / caretPositionFromPoint / caretRangeFromPoint
- *(cssom)* resolved used insets for positioned boxes + named window globals
- *(dom,js)* namespace lookup, DocumentType/PI, CSS.escape selector parsing, Attr/NamedNodeMap, DOMTokenList reflections
- *(engine)* overlay scrollbar on the right edge for overflowing pages
- *(dom,js)* real cloneNode, textContent, ChildNode/ParentNode mixins, fragments
- *(webdriver)* W3C WebDriver server to drive the engine over HTTP
- *(style,engine)* implement CSS color-scheme for dark UA defaults
- *(style,layout,engine)* border-collapse + HTML presentational table attributes
- *(theme)* prefers-color-scheme reflects the real macOS appearance
- *(dom)* img width/height attrs + alt, naturalWidth/Height, dialog API, textarea/select .value
- *(engine,layout)* render inline <svg> (was a 0x0 box, zero graphics)
- *(forms)* render input/progress/meter as real widgets; label hit box
- *(style,layout,paint)* block-level default rendering (margins, br, pre, hr, list markers)
- *(style,layout,paint)* default styling for inline text elements
- real Canvas 2D context (display list in JS, rasterized + composited by the engine)
- *(js,engine)* real window.scrollTo/scrollBy + element.scrollIntoView (were no-ops)
- *(net,js)* real WebSocket client via tungstenite (was a no-op stub)
- real getBoundingClientRect + offsetWidth/Height/Top/Left, clientWidth/Height, scrollWidth/Height, getClientRects
- *(devtools)* Elements DOM inspector tab (tree view + click-to-highlight on page)
- page text selection (drag to select, highlight, ⌘C copy)
- proper caret bar (not '|' glyph) + clickable <select> dropdowns (NSMenu)
- progressive/streaming first paint (Phase 1) — paint HTML as it downloads
- *(js,engine)* functional MutationObserver / IntersectionObserver / ResizeObserver
- *(swift,engine)* Chrome-like DevTools — Console (REPL) + Network tabs (⌘⌥I)
- *(net,engine,ffi)* devtools backend — network log + console REPL eval
- *(js,engine)* async concurrent fetch (background request threads + drain resolution)
- *(css,style,engine)* linear/radial gradients, box-shadow, transform (translate/scale/rotate)
- *(net,js)* FormData + fetch with method/headers/body (net::request)
- *(css,style)* full selector engine — combinators, pseudo-classes, attribute selectors
- mousedown/mouseup/dblclick/contextmenu events (Engine::dispatch_mouse)
- checkboxes/radios, change/focus/blur/submit, hover events, text caret
- live JS event loop — pump timers/animations after load (Engine::tick)
- text form input — typing, value rendering, input/keydown events; fix load race
- interactive pages — persistent per-tab JS runtime + click dispatch
- *(style,engine)* media/container queries + vw/vh use real viewport+DPR (responsive on resize)
- *(js,engine)* real devicePixelRatio + innerWidth/innerHeight from engine viewport
- *(js,engine)* run multi-MB scripts; add createHTMLDocument, Event family, DOM interface globals
- *(css,engine)* follow @import (recursive fetch) + CSS nesting (&)
- *(js,engine)* on-demand module fetch for dynamic import (referrer-relative resolve)
- *(engine,js)* ES module support (<script type=module> + import graph via Boa)
- *(engine,ffi,app)* tab titles from <title>; default homepage browserscore.dev
- *(css)* max/min sizing, line-height, text-transform, text-decoration, opacity, border-radius, logical props
- *(layout,engine,ffi,app)* clickable links (hit-test <a href> -> navigate)
- *(css,style)* apply @layer rules + parse rgb()/hsl()/oklch()/var(); drop debug bar
- *(engine)* decode data: URL images (base64 + percent-encoded)
- *(paint,layout,engine)* render <img> images (fetch, decode, blit)
- *(engine,ffi,app)* mouse-wheel scrolling for page content
- *(engine)* pipeline orchestration, paint, scripts, external resources

### Fixed

- *(style)* fully-transparent background-color is no background
- *(engine)* SVG currentColor resolves to the element color, not inherited fill/stroke
- *(js)* fire <body onload> on the window (Window-reflecting body handlers)
- *(svg)* parse packed path numbers; prefer url() background layer
- *(engine)* default to a proportional sans-serif font, not monospace
- *(engine)* scale page layout by the backing scale on HiDPI/Retina ([#88](https://github.com/suveshmoza/browser/pull/88))
- *(css,style)* resolve url() against the stylesheet's own URL, not the document
- *(engine,style)* default page canvas to white + black text (was a dark gradient)
- render <details>/<summary> + other block elements; click summary to toggle
- *(font)* prefer modern Unicode-cmap fonts (SF) over Monaco — fixes ·/é/α/→/€ rendering
- *(js)* Headers + URLSearchParams entries/keys/values iterators (fixes imlunahey.com)
- *(dom,engine)* prune out-of-bounds node ids after JS (renderer can't hit stale ids)
- *(engine)* collect stylesheets after scripts/modules (capture runtime-injected CSS)
- *(net)* shared connection-pooling agent (fix DNS failures from concurrent fetches)
- *(js)* innerHTML getter serializes real markup (Vue reads it as template)
- *(engine)* remove hardcoded page inset (margin/padding come from CSS)

### Other

- extract the URL parser into a shared `wurl` crate; drop url from all crates
- satisfy rustfmt and clippy (-D warnings)
- *(engine)* cap concurrent image fetches at 5
- split monolithic lib.rs files into focused modules ([#59](https://github.com/suveshmoza/browser/pull/59))
- green up the cross-platform matrix (exclude ffi on Linux/Windows; clippy 1.96) ([#2](https://github.com/suveshmoza/browser/pull/2))
- format workspace with rustfmt + make clippy clean (enforced in CI)
- *(engine)* cull offscreen subtrees in paint (don't walk the whole DOM per frame)
- Merge branch 'worktree-agent-abdcecdd6c488230d'
- Merge branch 'worktree-agent-a6a5029fc54f09d69'
- *(engine)* fetch ES module graph level-by-level in parallel
- *(engine,app)* cache layout so scrolling is paint-only; debounce resize
- *(engine)* fetch network images concurrently across a scoped thread pool
- *(engine)* add reveal/error diagnostic example for real-site debugging

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.0](https://github.com/suveshmoza/browser/compare/v0.0.2...v0.2.0) - 2026-07-02

### Added

- *(cookies)* Cookie Store API + assorted WPT fixes (cookiestore 0 → 70/74) ([#123](https://github.com/suveshmoza/browser/pull/123))
- honor the CORS credentials mode for cookies
- *(net)* return 4xx/5xx as responses and don't follow preflight redirects
- *(net)* expose response headers and status text to fetch/XHR
- *(cookies)* shared jar with prefix/Secure/SameSite rules and window.open contexts ([#117](https://github.com/suveshmoza/browser/pull/117))
- self.crossOriginIsolated from COOP+COEP response headers
- *(engine)* site favicons in the tab and address bar
- *(net)* URL fixup, HSTS, and http fallback in the engine (not the shell)
- *(wpt)* run conformance via real wpt serve + WebDriver (like other browsers) ([#80](https://github.com/suveshmoza/browser/pull/80))
- *(net,js)* real WebSocket client via tungstenite (was a no-op stub)
- progressive/streaming first paint (Phase 1) — paint HTML as it downloads
- *(net)* persistent cookie jar (stay logged in across requests + redirects)
- *(net,engine,ffi)* devtools backend — network log + console REPL eval
- *(net,js)* FormData + fetch with method/headers/body (net::request)
- *(net)* HTTP + file:// fetch via ureq with a browser User-Agent

### Fixed

- *(net)* don't let default Accept/Accept-Language shadow caller headers
- *(net)* preserve post-redirect final_url across disk-cache hits ([#109](https://github.com/suveshmoza/browser/pull/109))
- *(net)* report the post-redirect URL as final_url
- *(net)* tolerate unclean TLS close (no close_notify) on body read
- *(net)* asymmetric retry — fast status retries, stalls fail fast (no load freeze)
- *(net)* retry 403/429/5xx + transient errors with backoff; opt-in disk cache
- *(net)* shared connection-pooling agent (fix DNS failures from concurrent fetches)
- *(net,js)* request timeout + bounded module execution (no hang on heavy SPAs)

### Other

- cargo fmt
- extract the URL parser into a shared `wurl` crate; drop url from all crates
- green up the cross-platform matrix (exclude ffi on Linux/Windows; clippy 1.96) ([#2](https://github.com/suveshmoza/browser/pull/2))
- format workspace with rustfmt + make clippy clean (enforced in CI)
- *(net)* cache to per-user OS dir; drop committed cache + demo fixtures

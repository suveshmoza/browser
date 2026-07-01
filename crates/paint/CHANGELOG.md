# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.0](https://github.com/suveshmoza/browser/compare/v0.1.0...v0.2.0) - 2026-07-01

### Added

- *(js)* dedicated Web Workers (per-realm) and OffscreenCanvas
- *(css)* clip overflow:hidden content
- *(css)* max/min sizing, line-height, text-transform, text-decoration, opacity, border-radius, logical props
- *(paint,layout,engine)* render <img> images (fetch, decode, blit)
- *(paint,dom)* RGBA framebuffer compositor and arena DOM

### Other

- format workspace with rustfmt + make clippy clean (enforced in CI)

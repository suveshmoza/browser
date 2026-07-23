# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.0](https://github.com/suveshmoza/browser/compare/v0.1.0...v0.2.0) - 2026-07-23

### Added

- *(svg)* SVG IDL conformance — idlharness.window.html to 100% ([#119](https://github.com/suveshmoza/browser/pull/119))
- *(html)* in-body auto-closing for p / li / dd / dt / option / headings
- *(css,cssom)* namespace selector matching, @property, font-face rules, shorthand/all serialization
- *(dom,js)* namespace lookup, DocumentType/PI, CSS.escape selector parsing, Attr/NamedNodeMap, DOMTokenList reflections
- *(html)* always synthesize html>head+body skeleton (document.body never null)
- 279 HTML named entities + CSS ::before/::after generated content
- progressive/streaming first paint (Phase 1) — paint HTML as it downloads
- *(html)* hand-written HTML tokenizer and tree builder

### Fixed

- *(dom)* add DocumentFragment getElementById ([#83](https://github.com/suveshmoza/browser/pull/83))

### Other

- format workspace with rustfmt + make clippy clean (enforced in CI)

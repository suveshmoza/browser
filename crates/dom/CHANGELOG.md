# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.1.1](https://github.com/suveshmoza/browser/compare/v0.0.0...v0.1.1) - 2026-06-23

### Added

- *(dom)* CharacterData methods, CDATASection, and arena-backed off-documents ([#3](https://github.com/suveshmoza/browser/pull/3))
- *(css,cssom)* namespace selector matching, @property, font-face rules, shorthand/all serialization
- *(dom,js)* namespace lookup, DocumentType/PI, CSS.escape selector parsing, Attr/NamedNodeMap, DOMTokenList reflections
- *(dom,js)* real cloneNode, textContent, ChildNode/ParentNode mixins, fragments
- *(paint,dom)* RGBA framebuffer compositor and arena DOM

### Fixed

- *(dom,engine)* prune out-of-bounds node ids after JS (renderer can't hit stale ids)

### Other

- format workspace with rustfmt + make clippy clean (enforced in CI)

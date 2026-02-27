# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2025-02-27

### Added

- Batch compare: query multiple skills in one go and display stats side by side.
- Search by keyword: find skills by keyword and list their stats.
- `python3` declared in `metadata.openclaw.requires.bins` for completeness.
- README with installation, usage, and API reference.
- CHANGELOG to track version history.

### Changed

- Simplified SKILL.md frontmatter to follow official OpenClaw format (`name`, `description`, `metadata` only).
- Improved description to include detailed "Use when" trigger conditions.

## [1.0.0] - 2025-02-27

### Added

- Initial release.
- Single skill stats query via ClawHub public API (`GET /api/skill?slug={slug}`).
- Displays: stars, downloads, current installs, all-time installs, comments, versions.

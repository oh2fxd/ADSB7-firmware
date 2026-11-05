# Changelog

## [0.1.5] - 2026-11-05
- Built from commit c0906d7
- Fix map black-square: retry basemap tiles on transient fetch/decode failure,
  seed the composition buffer from the last published frame (a failed tile keeps
  its previous pixels instead of rendering black), and honour the tile fetch
  timeout in http_get_binary so slow downloads are not truncated into an
  undecodable PNG.

## [0.1.4] - 2026-10-16
- Built from commit aae3dd3

## [0.1.3] - 2026-09-17
- Built from commit dc2745f

## [0.1.2] - 2026-09-17
- Built from commit 75ad70a


# Changelog

## [0.1.29] - 2026-11-06
- Radar-only HUD: uniform amber + font size for clock, aircraft tags and LOC/IP; METAR forced visible top-left (station EFKI once fetched); clock without seconds. Secondary UI layout inspired by mircemk (Mirko Pavleski); implementation original (owner + AI).
- Built from commit 343ad41

## [0.1.28] - 2026-11-05
- Secondary (left-radar) UI polish: per-row aircraft list (plane icon + COUNTRY/CALL/DIST/ALT/SPD metric, even columns, Montserrat), 3-card bottom (centered amber clock, METAR, LOC+IP values in amber); radar-only view: clock without seconds + amber, SYS/SSID removed, METAR top-left and LOC/IP bottom-left at a uniform HUD font. Secondary UI layout inspired by mircemk (Mirko Pavleski); implementation original (owner + AI).
- Built from commit 9f863d2
## [0.1.16] - 2026-11-05
- Reference-style secondary UI (left radar + right DETECTED AIRCRAFTS panel: metric aircraft table, LOC, METAR, admin IP, large clock); monospace list font; revert to tear-free FULL render mode. Secondary UI layout inspired by mircemk (Mirko Pavleski) hackster ESP32 ADS-B radar; implementation original (owner + AI).
- Built from commit ceabef6
## [0.1.13] - 2026-11-05
- Remove ripple; add web-config option: left-aligned radar + right-side live aircraft list/stats (reboots on layout change)
- Built from commit 5a141a9
## [0.1.12] - 2026-11-05
- Smoother sweep: pclk 20->24MHz, throttle web/OTA handlers off the frame loop; ripple now a filled fading disc; remove diagnostic counter
- Built from commit 49f2628
## [0.1.11] - 2026-11-05
- DIAGNOSTIC: force ripple per rotation + HUD AC/PINGS counter to isolate why pings dont show
- Built from commit 750e1ce
## [0.1.10] - 2026-11-05
- More visible sonar ping: bigger/longer/thicker ring, ease-out fade, force ripple above aircraft layer
- Built from commit 94e7625
## [0.1.9] - 2026-11-05
- Inset sweep beam/head endpoints from radar edge to kill once-per-rotation gray bar blip
- Built from commit a4064e9
## [0.1.8] - 2026-11-05
- Fix OTA rollback (mark app valid on healthy boot) + auto-sync FW_VERSION; includes framebuffer-clear, sweep throttle, sonar-ping ripples
- Built from commit 073849c
## [0.1.7] - 2026-11-05
- Display fixes + sonar-ping radar: clear framebuffers (kill right-edge flash), throttle sweep to refresh rate, expanding ripple ping on sweep contact
- Built from commit 5dc8912
## [0.1.6] - 2026-11-05
- Add GitHub pull-OTA (check manifest + flash from web portal); map black-square fix
- Built from commit b2fe355
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


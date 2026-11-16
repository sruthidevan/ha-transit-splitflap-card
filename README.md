# Transit Split-Flap Card for Home Assistant

A transit-focused adaptation of [RazManSource/splitflap-card](https://github.com/RazManSource/splitflap-card). It keeps the split-flap animation and adds monochrome scramble defaults, configurable header-row color, and fixed board height for kiosk displays.

The upstream MIT license is retained in `LICENSE`. This card registers as `custom:transit-splitflap-card`, so it can coexist with the original card.

## Install with HACS

In HACS, add this repository as a custom repository and select the **Dashboard** category. Install it, then add its JavaScript resource if HACS does not add it automatically.

## YAML options

```yaml
type: custom:transit-splitflap-card
entity: sensor.transit_departures
title: Tram departures
rows: 4
columns: 32
line_separator: "|"
word_wrap: false
board_height: 72vh
header_rows: [0]
header_color: "#f5c542"
background_color: "#050505"
bar_style: off
color_mode: default
scramble_colors: ["#2c2c2c"]
animation: true
scramble_duration: 500
stagger_delay: 12
sound: false
```

The card displays the configured entity state. Use a template sensor or helper to format multiple rows, separated by the configured `line_separator`.

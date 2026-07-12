# Changelog

All notable changes to this fork are documented here. This project is a fork of
tuya-local; entries below cover changes made in the fork.

## 2026.7.2 - 2026-07-07

### Added
- Support for the **Thermex Boss 12 Wi-Fi** electric boiler (product id
  `jqmuspt7zb9b9n7c`, category `bgl`): climate control (on/off, target/current
  heating temperature, user/activity/sleep preset, heating status), plus
  activity/sleep setpoints, hysteresis, heating and pump times, heating type
  (radiator/floor), antifreeze switch, boiler power sensor and a fault
  diagnostic sensor with decoded error bits.

## 2026.7.1 - 2026-07-07

### Changed
- Merged upstream tuya-local **2026.7.0**, bringing in the latest device
  configs, translations and fixes. The fork's own additions and changes are
  kept on top (rebranding, the `device_config.py` Python 3 fix, and the Barista
  CFX-A01R, generic IR air conditioner and FBP-95E-GR profiles). Version set to
  2026.7.1 to stay one ahead of upstream.

## 2026.6.8 - 2026-06-29

### Added
- Support for the **FBP-95E-GR** fan (product id `enxohlgemolf1cqy`): on/off,
  preset mode (normal/nature/sleep), speed (1–12), horizontal oscillation, plus
  anion (ionizer) and beep switches and a countdown timer.

## 2026.6.7 - 2026-06-29

### Fixed
- **Critical:** `helpers/device_config.py` used a Python 2 `except TypeError,
  ValueError:` clause, which is a `SyntaxError` under Python 3. It prevented the
  config-matching module from importing at all, so no device could be detected
  or recognised. Replaced with `except (TypeError, ValueError):`.

## 2026.6.6 - 2026-06-29

### Added
- Support for a generic Tuya **IR-hub air conditioner** (category
  `infrared_ac`): climate entity with power, mode (cool/heat/auto/fan/dry),
  target temperature (16–30 °C), fan speed (auto/low/medium/high) and swing,
  plus `remote` and `infrared` entities for raw IR send/learn. Mode and fan
  codes follow the Tuya standard infrared_ac instruction set. Note: IR control
  is one-way, so reported state reflects the last command, not the AC itself.

## 2026.6.5 - 2026-06-29

### Added
- Support for the **Barista CFX-A01R** coffee machine (product id
  `wwt2piakfupgvrtd`): power, start/stop and brew controls, brewing mode
  selection, per-recipe powder/flow/temperature/water settings, maintenance and
  calibration switches, cups counter, firmware version and a fault diagnostic
  sensor with decoded error bits.

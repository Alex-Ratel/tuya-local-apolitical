# Changelog

All notable changes to this fork are documented here. This project is a fork of
tuya-local; entries below cover changes made in the fork.

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

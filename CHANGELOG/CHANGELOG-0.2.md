# Changelog 0.2

## [0.2.1](https://github.com/project-cdim/performance-exporter-compose/compare/v0.2.0...v0.2.1) - 2026-10-09

The changes from v0.2.0 are as follows:

### Features

- Added logger configuration files (`logger_settings_app.yaml`, `logger_settings_trail.yaml`) to configure the log tag and output type.

### Breaking Changes

- Updated required Go version from 1.24+ to 1.26+.
- Changed `compose.yml` to be generated from `compose.yml.template` at installation, with proxy settings taken from the common configuration file (`cdim.env`).

## [0.2.0](https://github.com/project-cdim/performance-exporter-compose/compare/v0.1.1...v0.2.0) - 2026-03-24

The changes from v0.1.1 are as follows:

### Features

- Fixed to retrieve devicePortList in metrics

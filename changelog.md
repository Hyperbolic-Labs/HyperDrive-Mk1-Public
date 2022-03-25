# Changelog
All notable changes to firmware will be documented in this file.



## [0.1.0] - 2022-03-12
### Added
- Initial Beta release
  
  

## [0.1.1] - 2022-03-16
### Added
- Normal mode (no wifi, less power consumption)
- Shutdown mode
- Automatic firmware selection based on programmed H/W rev
- Wake up from sleep with trigger pull
- Reduced power consumption on normal mode
- Automatic LiPo detection - 2S, 3S, and 4S

### Changed

### Removed
- LiPo series cells input (for low voltage cutoff)

### Fixed
- Low voltage cutoff sometimes unreliable
- Current measurements & cycle duration not displayed
- Battery voltage readout incorrect

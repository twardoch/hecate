# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased] - 2026-07-05

### Added
- `.gitignore` covering build output (`build/`, `.build_release/`, `distribute/`, `*.o`, `*.d`), editor/OS cruft (`.DS_Store`, `.vscode/`, `.dccache`), generated `output/`, and the `llms.txt` snapshot.
- Project icon at `docs/assets/icon.png`.

### Changed
- Rewrote README following the house style guide: clear fork provenance pointing at `yahoo/hecate`, a dedicated macOS/Homebrew build section, and the clone URL corrected to this fork.

## [v1.2.0] - 2022-10-04

### Added
- Docker support for easier installation and deployment (#36)
  - Added `docker/base.Dockerfile` with Debian Buster base image
  - Includes OpenCV 3.3.1 and FFmpeg integration
  - Added `docker/build.sh` script for automated Docker builds
  - Docker documentation in `docker/README.md`

## [v1.1.0] - 2020-2022

### Fixed
- Bug in sbd heuristic: `v_srt_val[i]` changed to `v_srt_idx[i]` (#10)
- Calculation of `len` for start and end in shot boundary detection
- Error handling when input file names contain empty spaces (#7)
- Error when there is only 1 data point in gap statistics (#2)
- Bug when using `--max_duration` parameter - now correctly limits frame reading (#19)

### Changed
- Updated `ffmpeg_helper.hpp` for better FFmpeg compatibility (#14)
- Improved backwards compatibility

### Contributors
- @KarenkovID - Shot boundary detection fixes
- @DatHuynh - Empty space filename handling
- @liuyang1 - Single data point error fix
- @vc60er - Max duration parameter fix
- @yalesong - FFmpeg helper updates
- @Nanne - Backwards compatibility improvements
- @smandal047 - Docker support
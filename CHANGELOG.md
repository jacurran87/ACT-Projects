# Changelog

All notable changes to **ACT Projects** will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Versions follow a date-based scheme (`YYYYMMDD`).

## [20260728] - Update

### Added
- **ACT-LensBlur.fuse** — new tool. A blur filter that simulates realistic depth of field and bokeh effects. This tool offers customization of the bokeh shape and features built-in chromatic aberration to mimic real-world lens imperfections with support for both blur maps or depth maps to enables precise variable blur distribution.
- **ACT-StylizedBlur.fuse** — new tool. A color-selective blur filter that creates a stylized blur effect. By selecting specific colors, the tool applies blur onto those colors, which then progressively sharpens as it moves outward toward the edges of the selected colors with support for blur map to enables custom control of blur distribution.
- **ACT-VariableBlur.fuse** — new tool. A Gaussian blur filter that supports blur map input to enable variable blur distribution across the image.

### Changed
- Renamed `SimpleAntiAliasing.fuse` to **`ACT-SimpleAntiAliasing.fuse`**, also updated to **v1.1**. See details below.

### ACT-SimpleAntiAliasing.fuse v1.1
- **Added:**
  - New `ACTSAA_EdgeKernel` precompute pass that calculates the edge map once at the start of the pipeline, instead of recalculating it inside every Seed/Grow iteration.
  - New `ACTSAA_OverlayKernel` for the "Edge Mask" view mode, rendering a proper red-on-dimmed-image overlay instead of the raw mask texture.
  - Logo, version label, and a new "Info" control page (description, Repository button, Socials button).
  - New registration flags for cleaner UI: `REG_NoObjMatCtrls`, `REG_Fuse_NoEdit`, `REG_Fuse_NoReload`, `REG_Version`.
- **Changed:**
  - Grow/Seed kernels now read from the precomputed `EdgeMap` instead of recomputing diffs every pass, cutting redundant GPU work at high Search Limit values.
  - All kernels and the params struct renamed with the `ACTSAA_` prefix, matching the naming convention used across other ACT tools. This changes also preventing conflict with any other fuses.
  - `REGS_Category` moved from `ACTProjects` to `ACTProjects\Image` for better organization; `REGS_OpIconString` changed from `SAA` to `ACT-SAA` for easier search through Fusion's Select Tool.
  - Reordered controls so "View Mode" appears before "Threshold".
- **Fixed:**
  - "Edge Mask" view mode no longer shows the black background and changed to source image for easier control.

## [20260303] - Initial release

### Added
- **SimpleAntiAliasing.fuse v1.0** — new / first tool. Smooths out jagged edges by detecting high-contrast pixels and blending them along the edge line.
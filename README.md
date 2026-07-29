# ACT PROJECTS

**ACT Projects** (Abi's Custom Tools) is a DaVinci Resolve / Fusion custom tools project for animation compositing.

### **[Download](https://github.com/AbiYasidAlMajid/ACT-Projects/releases)** | **[User Manual](ACTProjects-UserManual.pdf)** | **[Changelog](CHANGELOG.md)**

## Available Tools
Currently, the project includes the following tools:

### Lens Blur

<img width="1500" height="500" alt="ACT-LensBlur" src="https://github.com/user-attachments/assets/0c21f86d-26d7-407d-9d52-2508e677b7c1" />

A blur filter that simulates realistic depth of field and bokeh effects. This tool offers customization of the bokeh shape and features built-in chromatic aberration to mimic real-world lens imperfections with support for both blur maps or depth maps to enables precise variable blur distribution.

### Stylized Blur

<img width="1500" height="500" alt="ACT-StylizedBlur" src="https://github.com/user-attachments/assets/0b602efd-fc29-4b18-95cc-6ce1ba3fa460" />

A color-selective blur filter that creates a stylized blur effect. By selecting specific colors, the tool applies blur onto those colors, which then progressively sharpens as it moves outward toward the edges of the selected colors with support for blur map to enables custom control of blur distribution.

### Variable Blur

<img width="1500" height="500" alt="ACT-VariableBlur" src="https://github.com/user-attachments/assets/082f7f99-3f52-46dc-96b7-1be997948679" />

A Gaussian blur filter that supports blur map input to enable variable blur distribution across the image.

### Simple Anti-Aliasing

<img width="1500" height="500" alt="ACT-SimpleAntiAliasing" src="https://github.com/user-attachments/assets/c81a9389-4df4-4170-84c8-6184f4516339" />

Smooths out jagged edges by detecting high-contrast pixels and blending them along the edge line.

*(More tools will be added in future updates)*

## Requirements
- DaVinci Resolve 18.0 or later
- Fusion Studio 18.0 or later

## Installation
1. Download the tools.
2. Copy all the `.fuse` files into your "Fuses" directory:
   
   **DaVinci Resolve:**
   - **Windows:** `C:\ProgramData\Blackmagic Design\DaVinci Resolve\Support\Fusion\Fuses`
   - **macOS:** `~/Library/Application Support/Blackmagic Design/DaVinci Resolve/Support/Fusion/Fuses`
   - **Linux:** `~/.local/share/DaVinciResolve/Fusion/Fuses`
   
   **Fusion:**
   - **Windows:** `C:\ProgramData\Blackmagic Design\Fusion\Fuses`
   - **macOS:** `~/Library/Application Support/Blackmagic Design/Fusion/Fuses`
   - **Linux:** `~/.fusion/BlackmagicDesign/Fusion/Fuses`
3. Restart DaVinci Resolve / Fusion Studio.

## Copyright, License, and Contribute
This software is open-source and licensed under the **[MIT License](LICENSE)**. 
Feel free to reach out, report issues, or contribute to improving this software through GitHub pull requests.
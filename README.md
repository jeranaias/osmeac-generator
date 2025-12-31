# OSMEAC Generator

**Offline-capable 5-paragraph order builder for USMC tactical leaders.**

A progressive web app (PWA) that helps squad leaders, platoon commanders, and OCS candidates build standardized OSMEAC 5-paragraph orders with guided prompts and tactical night mode.

## Features

- **Complete OSMEAC Structure**: All 6 sections with line-by-line prompts
  - **O**rientation (KOCOA terrain analysis)
  - **S**ituation (SALUTE, DRAW-D, EMLCOA/EMDCOA)
  - **M**ission (5 W's format with tactical task dropdown)
  - **E**xecution (Commander's Intent, Tasks, Coordinating Instructions)
  - **A**dmin & Logistics (CASEVAC, resupply)
  - **C**ommand & Signal (PACE, call signs, challenge/password)

- **Tactical Night Mode**: Red on black display for field use - preserves night vision adaptation

- **100% Offline Capable**: Works without internet connection once installed

- **PWA Installable**: Add to home screen on mobile devices

- **Export & Print**: Save orders as text files or print formatted copies

- **Save/Load Orders**: Store multiple orders locally for reference

## Usage

1. Visit the app URL or install as PWA
2. Click on each section (O-S-M-E-A-C) to build your order
3. Fill in the guided prompts for each subsection
4. Preview your complete order
5. Export to text or print as needed

### Theme Modes

- **Light Mode**: Standard daytime use
- **Dark Mode**: Low-light environments
- **Night Mode**: Tactical red-on-black for field operations

Toggle themes using the sun/moon icon in the header.

## Acronyms Reference

### OSMEAC
- **O**rientation
- **S**ituation
- **M**ission
- **E**xecution
- **A**dministration & Logistics
- **C**ommand & Signal

### KOCOA (Terrain Analysis)
- **K**ey terrain
- **O**bservation & fields of fire
- **C**over & concealment
- **O**bstacles
- **A**venues of approach

### SALUTE (Enemy Report)
- **S**ize
- **A**ctivity
- **L**ocation
- **U**nit/Uniform
- **T**ime observed
- **E**quipment

### DRAW-D (Enemy Capabilities)
- **D**efend
- **R**einforce
- **A**ttack
- **W**ithdraw
- **D**elay

## Installation

### As a PWA (Recommended)
1. Open the app in Chrome, Edge, or Safari
2. Click "Add to Home Screen" or install from browser menu
3. App works offline once installed

### Self-Hosted
```bash
git clone https://github.com/jeranaias/osmeac-generator.git
cd osmeac-generator
# Serve with any static file server
npx serve .
```

## References

- MCRP 3-11.2 (Marine Rifle Squad)
- MCWP 5-10 (Marine Corps Planning Process)
- OCS 5-Paragraph Order guidance

## Community Attribution

This tool was built based on feedback from the r/USMC community:

| Contributor | Platform | Contribution |
|-------------|----------|--------------|
| **Alarming-Weekend-999** | r/USMC | Detailed spec request: offline, night mode (red/black), line-by-line prompts |

*This tool exists because Marines took the time to share their pain points. Thank you.*

## Part of USMC Tools

This generator is part of the [USMC Tools](https://jeranaias.github.io/usmc-tools/) suite - free, offline-capable web tools for Marine Corps administrative tasks.

## License

MIT License - See [LICENSE](LICENSE) file for details.

---

*Semper Fidelis*

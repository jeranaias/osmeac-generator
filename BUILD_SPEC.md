# OSMEAC Generator - Build Specification

## Overview

**Repo Name:** `osmeac-generator`
**Purpose:** Offline-capable 5-paragraph order builder with night mode (red on black), line-by-line prompts for each section, and exportable output. Designed for field use.
**Target Users:** Squad leaders, Platoon commanders, SNCO/NCO tactical leaders, OCS candidates

---

## Design System

**CRITICAL:** Use the shared design system from `DESIGN_SYSTEM.md`. All colors, typography, spacing, and components must match exactly for suite consistency.

**SPECIAL REQUIREMENT:** This tool MUST have a tactical night mode (red elements on black background) for field use. This was specifically requested.

---

## References

- MCRP 3-11.2 (Marine Rifle Squad)
- MCWP 5-10 (Marine Corps Planning Process)
- OCS 5-Paragraph Order guidance

---

## Background: OSMEAC / 5-Paragraph Order

### Structure
The 5-paragraph order uses the acronym **SMEAC**:
- **S**ituation
- **M**ission
- **E**xecution
- **A**dministration & Logistics
- **C**ommand & Signal

The Marine Corps adds **O**rientation at the beginning, making it **OSMEAC**.

### Purpose
Provides a standardized format for issuing tactical orders at all levels. Ensures all critical information is communicated to subordinates.

---

## Features Required

### 1. Orientation Section Builder
- Grid coordinate input (8-digit)
- Direction of movement (azimuth)
- Terrain analysis prompts (KOCOA)
- Weather conditions
- Terrain model notes

### 2. Situation Section Builder
- Enemy forces (SALUTE format)
- Enemy capabilities (DRAW-D)
- Most likely/most dangerous COA
- Friendly forces (Higher/Adjacent/Supporting)
- Attachments/Detachments

### 3. Mission Section Builder
- 5 W's format (Who, What, When, Where, Why)
- Task and purpose builder
- Mission statement generator

### 4. Execution Section Builder
- Commander's Intent (Purpose, Method, End State)
- Concept of Operations
- Scheme of Maneuver
- Fire Support Plan
- Tasks to subordinate units
- Coordinating instructions

### 5. Admin & Logistics Section Builder
- Ammunition
- Rations/Water
- Casualty evacuation (CASEVAC)
- EPW handling
- Resupply points

### 6. Command & Signal Section Builder
- Command structure/succession
- CP location
- Frequencies
- Call signs
- Signals/pyrotechnics
- Challenge/password

### 7. Special Features
- **Night Mode** (Red on black) - CRITICAL
- **100% Offline capable**
- **PWA installable**
- Export to PDF/text
- Print formatted order
- Save/load orders locally

---

## Acronyms & Frameworks

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

### EMLCOA / EMDCOA
- **E**nemy **M**ost **L**ikely **C**ourse **O**f **A**ction
- **E**nemy **M**ost **D**angerous **C**ourse **O**f **A**ction

### HAS-A (Friendly Forces)
- **H**igher's mission & intent
- **A**djacent units
- **S**upporting units
- **A**ttachments/Detachments

---

## Order Template Structure

### ORIENTATION
```
1. ORIENTATION

   a. Present Location: Grid [________] (8-digit)
   
   b. Direction of Attack: [___]° magnetic, [___] meters
   
   c. Objective Location: Grid [________] (8-digit)
   
   d. Terrain (KOCOA):
      (1) Key Terrain: [________________]
      (2) Observation & Fields of Fire: [________________]
      (3) Cover & Concealment: [________________]
      (4) Obstacles: [________________]
      (5) Avenues of Approach: [________________]
   
   e. Weather: [________________]
   
   "Are there any questions on the orientation?"
```

### I. SITUATION
```
I. SITUATION

   a. Enemy Forces:
      (1) Composition, Disposition, Strength (SALUTE):
          - Size: [________________]
          - Activity: [________________]
          - Location: Grid [________]
          - Unit/Uniform: [________________]
          - Time: [________________]
          - Equipment: [________________]
      
      (2) Capabilities (DRAW-D):
          - Defend: [________________]
          - Reinforce: [________________]
          - Attack: [________________]
          - Withdraw: [________________]
          - Delay: [________________]
      
      (3) EMLCOA: [________________]
      
      (4) EMDCOA: [________________]

   b. Friendly Forces:
      (1) Higher's Mission: [________________]
      (2) Higher's Intent: [________________]
      (3) Adjacent Units:
          - North: [________________]
          - South: [________________]
          - East: [________________]
          - West: [________________]
      (4) Supporting Units: [________________]

   c. Attachments/Detachments: [________________]
```

### II. MISSION
```
II. MISSION

    [WHO] [WHAT tactical task] [WHERE location/grid] NLT [WHEN time] 
    IOT [WHY purpose]
    
    Example:
    "1st Squad attacks to seize Building 4 at grid 12345678 NLT 0600 
    in order to establish a support-by-fire position for the platoon's 
    main assault."
```

### III. EXECUTION
```
III. EXECUTION

    a. Commander's Intent:
       (1) Purpose: [________________]
       (2) Method: [________________]
       (3) End State:
           - Friendly: [________________]
           - Enemy: [________________]
           - Terrain: [________________]

    b. Concept of Operations:
       (1) Scheme of Maneuver: [________________]
       (2) Fire Support Plan: [________________]

    c. Tasks to Subordinate Units:
       (1) 1st Fire Team: [WHO does WHAT, WHERE, WHEN, WHY]
       (2) 2nd Fire Team: [WHO does WHAT, WHERE, WHEN, WHY]
       (3) 3rd Fire Team: [WHO does WHAT, WHERE, WHEN, WHY]
       (4) Attachments: [________________]

    d. Coordinating Instructions:
       (1) Timeline: [________________]
       (2) Priority of Fires: [________________]
       (3) ROE: [________________]
       (4) MOPP Level: [________________]
       (5) Actions on Contact: [________________]
       (6) Actions at Objective: [________________]
       (7) Consolidation/Reorganization: [________________]
       (8) Movement Formation: [________________]
       (9) Movement Technique: [________________]
       (10) Departure/Reentry of Lines: [________________]
```

### IV. ADMINISTRATION & LOGISTICS
```
IV. ADMINISTRATION & LOGISTICS

    a. Administration:
       (1) EPW Handling: [________________]
       (2) Captured Material: [________________]

    b. Logistics:
       (1) Ammunition: [________________]
       (2) Rations: [________________]
       (3) Water: [________________]
       (4) Special Equipment: [________________]
       (5) Resupply Point: Grid [________]

    c. CASEVAC:
       (1) Collection Point: Grid [________]
       (2) Route: [________________]
       (3) Medical Support: [________________]
```

### V. COMMAND & SIGNAL
```
V. COMMAND & SIGNAL

    a. Command:
       (1) Location of Commander: [________________]
       (2) Succession of Command: [________________]
       (3) CP Location: Grid [________]

    b. Signal:
       (1) Frequencies:
           - Primary: [________________]
           - Alternate: [________________]
           - Contingency: [________________]
           - Emergency: [________________]
       (2) Call Signs:
           - Higher: [________________]
           - This Unit: [________________]
           - Subordinates: [________________]
       (3) Signals:
           - Shift Fire: [________________]
           - Cease Fire: [________________]
           - Assault: [________________]
           - Rally Point: [________________]
       (4) Pyrotechnics: [________________]
       (5) Challenge/Password: [________________]
       (6) Running Password: [________________]
       (7) Number Combination: [________________]

    "Are there any questions?"

    TIME HACK: [________________]
```

---

## UI Structure

### Main Screen
```
┌─────────────────────────────────────┐
│ ☀️/🌙  OSMEAC GENERATOR        [≡] │
├─────────────────────────────────────┤
│                                     │
│  ┌─────────────────────────────┐    │
│  │ O - Orientation        [>]  │    │
│  └─────────────────────────────┘    │
│  ┌─────────────────────────────┐    │
│  │ S - Situation          [>]  │    │
│  └─────────────────────────────┘    │
│  ┌─────────────────────────────┐    │
│  │ M - Mission            [>]  │    │
│  └─────────────────────────────┘    │
│  ┌─────────────────────────────┐    │
│  │ E - Execution          [>]  │    │
│  └─────────────────────────────┘    │
│  ┌─────────────────────────────┐    │
│  │ A - Admin & Logistics  [>]  │    │
│  └─────────────────────────────┘    │
│  ┌─────────────────────────────┐    │
│  │ C - Command & Signal   [>]  │    │
│  └─────────────────────────────┘    │
│                                     │
├─────────────────────────────────────┤
│ [New Order] [Load] [Export] [Print] │
└─────────────────────────────────────┘
```

### Section Screen (Example: Mission)
```
┌─────────────────────────────────────┐
│ [<] MISSION                    [?]  │
├─────────────────────────────────────┤
│ Build your mission statement using  │
│ the 5 W's:                          │
│                                     │
│ WHO (unit):                         │
│ [1st Squad________________]         │
│                                     │
│ WHAT (tactical task):               │
│ [attacks to seize________▼]         │
│                                     │
│ WHERE (location):                   │
│ [Building 4, Grid 12345678]         │
│                                     │
│ WHEN (time):                        │
│ [NLT 0600_______________]           │
│                                     │
│ WHY (purpose - starts with IOT):    │
│ [establish a support-by-fire        │
│  position for the platoon's main    │
│  assault___________________]        │
│                                     │
├─────────────────────────────────────┤
│ Generated Mission Statement:        │
│ ┌─────────────────────────────────┐ │
│ │"1st Squad attacks to seize      │ │
│ │Building 4 at grid 12345678 NLT  │ │
│ │0600 IOT establish a support-by- │ │
│ │fire position for the platoon's  │ │
│ │main assault."                   │ │
│ └─────────────────────────────────┘ │
├─────────────────────────────────────┤
│ [Previous]              [Next]      │
└─────────────────────────────────────┘
```

### Night Mode (Red on Black)
```
┌─────────────────────────────────────┐
│ 🌙  OSMEAC GENERATOR          [≡]  │  <- Red text
├─────────────────────────────────────┤  <- Black background
│                                     │
│  ┌─────────────────────────────┐    │  <- Dark red borders
│  │ O - Orientation        [>]  │    │  <- Red text
│  └─────────────────────────────┘    │
│  ┌─────────────────────────────┐    │
│  │ S - Situation          [>]  │    │
│  └─────────────────────────────┘    │
│  ...                                │
└─────────────────────────────────────┘
```

---

## Night Mode CSS

```css
[data-theme="night"] {
  --primary: #FF0000;
  --primary-dark: #CC0000;
  --primary-light: #FF3333;
  
  --bg-primary: #000000;
  --bg-secondary: #0A0000;
  --bg-tertiary: #140000;
  --surface: #0A0000;
  --surface-hover: #1A0000;
  
  --text-primary: #FF0000;
  --text-secondary: #CC0000;
  --text-tertiary: #990000;
  
  --border-light: #330000;
  --border-medium: #660000;
  --border-dark: #990000;
  
  /* All semantic colors become red for night vision */
  --success: #FF0000;
  --warning: #FF0000;
  --error: #FF3333;
  --info: #FF0000;
}

/* Ensure everything is truly black background */
[data-theme="night"] body {
  background: #000000;
}

[data-theme="night"] input,
[data-theme="night"] textarea,
[data-theme="night"] select {
  background: #0A0000;
  color: #FF0000;
  border-color: #660000;
}
```

---

## Tactical Tasks Dropdown

Common tactical tasks for the WHAT field:

```javascript
const tacticalTasks = [
  // Offensive
  "attacks to seize",
  "attacks to destroy",
  "attacks to neutralize",
  "attacks to secure",
  "attacks to clear",
  "conducts a raid on",
  "conducts an ambush at",
  "infiltrates to",
  "breaches",
  "bypasses",
  "envelops",
  "penetrates",
  "turns",
  
  // Defensive
  "defends",
  "delays",
  "withdraws to",
  "retrogrades to",
  "blocks",
  "contains",
  "disrupts",
  
  // Security
  "screens",
  "guards",
  "covers",
  "conducts area security of",
  
  // Other
  "reconnoiters",
  "occupies",
  "secures",
  "seizes",
  "holds",
  "supports by fire",
  "provides overwatch of",
  "establishes a blocking position at"
];
```

---

## Technical Implementation

### Files
```
osmeac-generator/
├── index.html
├── manifest.json
├── service-worker.js
├── css/
│   ├── styles.css
│   └── night-mode.css      # Critical for field use
├── js/
│   ├── app.js
│   ├── sections/
│   │   ├── orientation.js
│   │   ├── situation.js
│   │   ├── mission.js
│   │   ├── execution.js
│   │   ├── admin-logistics.js
│   │   └── command-signal.js
│   ├── tactical-tasks.js   # Task dropdown options
│   ├── export.js           # PDF/text export
│   ├── theme.js            # Theme management
│   └── storage.js          # Save/load orders
├── assets/
│   ├── icon-192.png
│   └── icon-512.png
├── README.md
└── LICENSE
```

### Key Functions

```javascript
// Build mission statement from 5 W's
function buildMissionStatement(who, what, where, when, why) {
  return `${who} ${what} ${where} NLT ${when} IOT ${why}.`;
}

// Generate complete order
function generateOrder(orderData) {
  const sections = [
    generateOrientation(orderData.orientation),
    generateSituation(orderData.situation),
    generateMission(orderData.mission),
    generateExecution(orderData.execution),
    generateAdminLogistics(orderData.adminLog),
    generateCommandSignal(orderData.cmdSig)
  ];
  return sections.join('\n\n');
}

// Export to text file
function exportToText(orderText, filename) {
  const blob = new Blob([orderText], { type: 'text/plain' });
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url;
  a.download = `${filename}.txt`;
  a.click();
}

// Toggle night mode
function toggleNightMode() {
  const current = document.documentElement.getAttribute('data-theme');
  const newTheme = current === 'night' ? 'light' : 'night';
  document.documentElement.setAttribute('data-theme', newTheme);
  localStorage.setItem('osmeac-theme', newTheme);
}
```

---

## Offline Capability (Critical)

The service worker MUST cache all assets for 100% offline use:

```javascript
const CACHE_NAME = 'osmeac-v1';
const urlsToCache = [
  '/',
  '/index.html',
  '/css/styles.css',
  '/css/night-mode.css',
  '/js/app.js',
  '/js/sections/orientation.js',
  '/js/sections/situation.js',
  '/js/sections/mission.js',
  '/js/sections/execution.js',
  '/js/sections/admin-logistics.js',
  '/js/sections/command-signal.js',
  '/js/tactical-tasks.js',
  '/js/export.js',
  '/js/theme.js',
  '/js/storage.js',
  '/assets/icon-192.png',
  '/assets/icon-512.png',
  '/manifest.json'
];

self.addEventListener('install', event => {
  event.waitUntil(
    caches.open(CACHE_NAME)
      .then(cache => cache.addAll(urlsToCache))
  );
});

self.addEventListener('fetch', event => {
  event.respondWith(
    caches.match(event.request)
      .then(response => response || fetch(event.request))
  );
});
```

---

## Testing Checklist

- [ ] All 6 sections (OSMEAC) navigate correctly
- [ ] Night mode fully functional (all red on black)
- [ ] Mission statement builder generates correctly
- [ ] Tactical tasks dropdown works
- [ ] All input fields save to order data
- [ ] Export to text works
- [ ] Print formatting correct
- [ ] Save/load orders from localStorage
- [ ] **100% offline capable** (critical)
- [ ] PWA installable
- [ ] Mobile responsive (phone primary use)
- [ ] Theme persists across sessions

---

## Future Enhancement: Android APK

User requested .apk for ATAK integration. Can be done with:
- Capacitor (recommended)
- Cordova
- PWA Builder

This is a stretch goal - focus on PWA first.

---

## Community Attribution

This tool was inspired by feedback from the r/USMC community:

| Contributor | Platform | Contribution |
|-------------|----------|--------------|
| **Alarming-Weekend-999** | r/USMC | Detailed spec request: offline, night mode (red/black), line-by-line prompts, .apk for ATAK |

*This tool exists because Marines took the time to share their pain points. Thank you.*

---

## Deployment

1. Push to GitHub repo `jeranaias/osmeac-generator`
2. Enable GitHub Pages from main branch
3. Test at `https://jeranaias.github.io/osmeac-generator/`
4. Test offline capability
5. Test night mode in dark environment

---

## Git Commit Guidelines

**IMPORTANT:** Do NOT include any Claude, Anthropic, or AI attribution in commit messages. Keep commits professional and human-authored in tone:

```
# GOOD commit messages:
git commit -m "Add night mode with red-on-black theme"
git commit -m "Implement OSMEAC section templates"
git commit -m "Add service worker for offline capability"

# BAD commit messages (do not use):
git commit -m "Generated by Claude..."
git commit -m "AI-assisted implementation of..."
```

---

*Spec Version 1.0 - December 2025*

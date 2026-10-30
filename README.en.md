# Lakaz Plan

*[Version française](README.md)*

Survey existing buildings before renovation: dimensioned floor plans, defects with photos, quantities and a PDF report. Built for non-specialist teams working in the field in the Seychelles.

**Open the app: https://myrdinevil.github.io/Lakaz-Plan/**

"Lakaz" means "house" in Seychellois Creole.

The app is available in English and French. It follows the phone's language, and you can switch at any time (Menu › Language).

## What it is for

Before renovating a run-down building, you need to know exactly what you are dealing with. Lakaz Plan produces:

- a scaled plan of each floor, showing wall thickness, doors and windows;
- a list of defects (cracks, spalling concrete, rusted rebar, damp, termites, roofing…) located on the plan, with photos, severity and recommended repairs;
- quantities for pricing the work: floor and wall areas, skirting lengths, volumes;
- a PDF report to hand over to the architect, the contractor or the owner.

## Installation

There is nothing to download or install.

### On iPhone

1. Open the link above in **Safari**. Chrome and the WhatsApp preview cannot install it.
2. Tap the Share button (the square with an upward arrow).
3. Choose "Add to Home Screen", then "Add".
4. Open the app once while connected to the internet. After that it works without a network.

### On Android

Open the link in Chrome, tap the ⋮ menu, then "Add to Home screen".

### On a computer

Open the link in any browser. You can also download this repository (green "Code" button › "Download ZIP") and double-click `index.html`: the app then runs fully offline.

## How to use it

1. **Draft.** Add rooms one by one (➕ button), or import a sketch as a background (🖼️) and trace over it (✏️), or let the AI read the sketch (✨).
2. **Measure.** Room by room, measure the walls and the diagonals. A diagram highlights in red what to measure next.
3. **Assemble.** Drag the rooms into place: they snap to each other, leaving room for the wall thickness.
4. **Doors, windows and defects.** Use the 🚪, 🪟 and ⚠️ tools. Photos can be added straight from the phone.
5. **Report.** "PDF report" tab, then "Print / Save as PDF". Keep the print scale at 100%.

A detailed user guide is built into the app: Menu › User guide.

## How accurate are the plans?

A photo or a sketch cannot give exact dimensions: the scale is unknown and perspective distorts everything. They only serve as a draft. Accuracy comes from measurements taken on site.

- With a laser distance meter (about €30) or a tape measure, you get to the centimetre.
- On an iPhone Pro, Apple's built-in Measure app uses the LiDAR sensor and can replace the laser meter (1 to 2 cm off).
- Diagonals are essential in old buildings, where corners are rarely square: they are what give the room its true shape. The check diagonal catches a wrong measurement.
- Until a dimension has been measured, it stays orange with a ≈ sign, both on the plan and in the report. The report states the share of dimensions actually measured on site.

## Data and backups

There is no account and no server. Surveys are stored on the device that created them and never leave it. The app link gives no access to anyone's data.

- Save the project file regularly: Menu › Save the project file. This `.lakaz.json` file contains everything, photos included. It is your backup.
- To share a survey with a colleague or the architect, send them this file (WhatsApp, email, USB stick). They open it with Menu › Open a project file.
- A survey on the computer and one on the phone are two separate copies: the project file is how you move between them.
- On iPhone, Safari may delete the data of a web page that has not been added to the Home Screen.

## AI analysis (optional)

The ✨ tool sends the selected images to Anthropic's Claude API, which suggests a draft: rooms, openings, visible defects. Every dimension it suggests is marked ≈ and must be measured.

It needs an internet connection and a personal API key (console.anthropic.com), billed per use: roughly $0.05 to $0.20 per analysis. The key is stored on the device only. The rest of the app works without internet and without a key.

## Exports

| Format | Content |
|---|---|
| PDF | Summary, scaled plans (1:50, 1:100…) with title block, north arrow and scale bar, quantities, defects with photos |
| CSV | Quantities and defects, to open in Excel |
| SVG | Floor plan at 1:100 scale, for use in drawing software |
| `.lakaz.json` | Complete project, for backup and sharing |

## Repository contents

| File | Purpose |
|---|---|
| `index.html` | The whole app, in a single file, with no dependencies |
| `sw.js` | Keeps the app on the phone for offline use |
| `manifest.webmanifest` | Name and icon for installing on the Home Screen |
| `icon.svg` | App icon |

## Updating the app

Edit `index.html`, then publish with GitHub Desktop ("Commit", then "Push origin"). The site updates within one or two minutes. Phones pick up the new version the next time they open the app with a network connection.

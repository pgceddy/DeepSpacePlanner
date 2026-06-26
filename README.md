# DeepSkyScanner

A free, open-source mobile web app for planning deep sky observation sessions with the **Seestar S50** smart telescope — or any similar instrument.

Point your iPad or phone at any region of sky to instantly see a list of deep sky objects in that field of view, with a circular eyepiece overlay showing their positions, visibility information, and imaging notes.

[Try it out](https://pgceddy.github.io/DeepSpacePlanner/)

-----

## Features

### 🔭 Live Sky Scanning

- Point your device at the sky in portrait mode (camera facing the sky, screen facing you)
- Real-time RA/Dec readout from device compass and tilt sensors
- Tap **Scan** to capture all deep sky objects within your chosen field of view
- Tap **Live** for continuous scanning as you sweep across the sky
- Tap **Find** to lookup specific object and review details

### 🕐 Planning Mode

- Tap **Plan** to activate the time slider
- Scrub from 5:00 PM to 2:00 AM in 15-minute increments
- See what objects will be in any region of sky at any time tonight
- Plan your entire session during the day before you go out

### 👁 Eyepiece Overlay

- Circular eyepiece view showing object positions relative to your pointing direction
- North up, East right — standard naked-eye sky orientation
- RA and Dec range labels on all four edges
- Zenith direction indicator (Z arrow) showing how the chart relates to your physical view
- Color-coded by object type: blue = galaxy, gold = globular cluster, green = open cluster, red = nebula
- Dot size reflects brightness — brighter objects appear larger
- Tap any dot to open the full detail sheet

### 📋 Object List

- Ranked by distance from scan center (nearest first) or magnitude (brightest first) or highest altitude (best first)
- Toggle sort with the **Nearest / Brightest / Best** button in the list header
- Shows object name, type, constellation, RA/Dec, magnitude, and separation from center

### 📖 Object Detail Sheet

- DSS2 color sky image from CDS/Aladin
- **Visibility Tonight** — rise time, best viewing time (peak altitude), set time, current altitude bar
  - Automatically uses plan time when in planning mode
  - Change plan time in detail sheet to see updated visibility information
  - Handles circumpolar objects correctly
- **About This Object** — description pulled from Wikipedia
- **Seestar S50 Notes** — practical imaging advice tailored to object type and brightness
- Full coordinate readout

### 🌐 Live Catalog

- Built-in curated catalog of ~400 Messier and NGC/IC objects
- Automatically enriched with additional objects from OpenNGC on load (requires network)
- Magnitude filter slider (6.0 to 14.0)
- Field of view slider (5° to 60°)

-----

## How to Use

### Basic Workflow

1. Open the app in Safari/Chrome on your iPad or iPhone
1. Grant compass and motion sensor permissions when prompted
1. Point the device camera at the region of sky you want to explore
1. Adjust the **FOV** and **MAG** sliders to match your session goals
1. Tap **Scan** — the eyepiece overlay and object list appear
1. Tap any object to see details, visibility, and imaging notes
1. Use **Lock** to freeze the current pointing as a snapshot

### Planning a Session

1. Point the device at the sky region you plan to image
1. Tap **Plan** to activate the time slider
1. Scrub the slider to the time you plan to observe
1. Tap **Scan** to see what’s available at that time
1. Adjust pointing direction and repeat to explore different sky regions
1. Use **Lock** to freeze a pointing for reference while you review

### Tips

- Hold the iPad in portrait mode with the camera facing the sky, like taking a photo
- The compass auto-corrects when tilting the iPad steeply upward
- Tap **Live** to keep the object list updating continuously as you move
- For high-declination targets near the pole, use **Plan + Lock** to avoid sensor instability
- The eyepiece dots are tappable — tap any object dot to open its detail sheet

-----

## Installation

DeepSkyScanner is a **Progressive Web App (PWA)** — a single HTML file with no dependencies, no installation required, and no app store needed.

### Option 1 — Use the hosted version

Visit the live URL (see Releases or the link in this repo description) in Safari on your iPhone or iPad.

### Option 2 — Add to Home Screen (recommended)

1. Open the app URL in Safari or Chrome
1. Tap the Share button → **Add to Home Screen**
1. The app installs like a native app with its own icon

### Option 3 — Self-host

Download `DeepSkyScanner.html` and host it anywhere — GitHub Pages, Netlify, your own server, or just open the file directly in a browser.

-----

## Device Requirements

- **iPhone or iPad** with Safari or Chrome (iOS 13+) — recommended for full compass and motion sensor support
- Android devices with Chrome should work but sensor behavior may vary
- Internet connection required for: SIMBAD catalog enrichment, sky images, Wikipedia descriptions

-----

## Compatibility

Designed and tested with the **Seestar S50** smart telescope. The field of view slider (5°–60°) covers the Seestar’s native FOV and mosaic modes. The Seestar S50 imaging notes in the detail sheet are tailored specifically to the S50’s capabilities.

Should be useful for any visual or imaging observer — the catalog, eyepiece view, and visibility calculations are telescope-agnostic.

-----

## Catalog Sources

- **Messier catalog** — built in, hand-curated with common names and descriptions
- **NGC/IC objects** — curated selection of ~280 objects, magnitude < 12
- **SIMBAD TAP service** — additional NGC/IC objects loaded at startup (CDS, Strasbourg)
- **Sky images** — DSS2 color via CDS HiPS2FITS service
- **Object descriptions** — Wikipedia REST API

-----

## Known Limitations

- iOS compass flips when tilting the iPad past ~134° beta angle — the app auto-corrects this but brief flicker may occur at the threshold
- Very high declination targets (>75°) near the zenith may show sensor instability in live mode — use Plan + Lock for these
- Rise/set times are approximate (5-minute resolution)
- SIMBAD enrichment and Wikipedia descriptions require an internet connection

-----

## Contributing

Bug reports, feature requests, and pull requests are welcome. Open an issue to discuss before submitting large changes.

Ideas for future development:

- Constellation boundary overlay on eyepiece
- Session log / target checklist
- Seestar integration via local network API
- Offline catalog expansion

-----

## License

MIT License — free to use, modify, and share. Attribution appreciated.

-----

## Acknowledgments

- Sky images: [CDS / DSS2](https://aladin.cds.unistra.fr)
- Catalog data: [SIMBAD Astronomical Database](https://simbad.u-strasbg.fr), CDS Strasbourg
- Object descriptions: [Wikipedia](https://wikipedia.org)
- Built for the Seestar S50 community

-----

*Clear skies!* 🔭

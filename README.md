# RavenC:LAW

**Ravenna Cosmography: Locations, Alignments & Weblinks**

An interactive spatial exploration platform for the 7th-century Ravenna Cosmography—a medieval geographic text describing places known to the Roman world.

## Features

- **Dual-map view**: Synchronized display of the Peutinger Map (historical) and modern geographic map
- **3,500+ ancient toponyms** from Books 1-5 of the Ravenna Cosmography
- **Hierarchical navigation**: Browse by Book → Region (Patria) → List → Place
- **Cross-references** to major ancient geography databases:
  - [Pleiades](https://pleiades.stoa.org/) - Ancient place gazetteer
  - [TP-Online](https://tp-online.ku.de/) - Peutinger Map digitization (Katholische Universität Eichstätt-Ingolstadt)
  - [Talbert Roman Geography](https://www.cambridge.org/us/talbert/) - Cambridge database
- **Littoral itinerary visualization**: Book 5's 14-stage coastal circuit around the Mediterranean
- **Multiple symbology modes**: Color by region, by list sequence, or by primary source
- **Search**: Find places by toponym name
- **Direct source links**: Click toponyms to view the Schnetz edition PDF at the relevant page

## Directory Color Coding

The place directory uses colors to indicate data completeness:

| Color | Meaning |
|-------|---------|
| 🟢 Green | Place matched in both TP-Online AND Pleiades |
| 🟠 Orange | TP-Online only (appears on Peutinger Map, no modern coordinates) |
| 🔵 Blue | Pleiades only (modern coordinates, not on Peutinger Map) |
| 🔴 Red | No coordinates available in either database |

## Map Symbols

- **Filled circles**: Places that appear on the Peutinger Map
- **Cross symbols (+)**: Places NOT on the Peutinger Map
- **Littoral stages**: Alternating black/white markers distinguish the 14 coastal circuit stages

## Data Sources

| Source | Description |
|--------|-------------|
| **Primary text** | Schnetz edition (1939-1940) of the Ravenna Cosmography |
| **Peutinger Map** | [TP-Online](https://tp-online.ku.de/) digitization by KU Eichstätt-Ingolstadt |
| **Geographic coordinates** | [Pleiades](https://pleiades.stoa.org/) ancient places gazetteer |
| **Base map** | [Digital Atlas of the Roman Empire](https://imperium.ahlfeldt.se/) (DARE) |
| **Historical boundaries** | Late Roman provinces/dioceses (AD 303), Euratlas polities (c. 600 AD) |

## Data Files

| File | Description |
|------|-------------|
| `ravenclaw.csv` | Main database of 3,500+ toponyms from Books 1-5 |
| `rc_littoral.csv` | Littoral (coastal) itinerary from Book 5 |
| `ku_tp_*.geojson` | Peutinger Map features (coastlines, rivers, mountains, etc.) |
| `*_paths.geojson` | Place sequence connections |
| `schnetz.pdf` | Schnetz edition of the Ravenna Cosmography |

## Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/leifuss/ravenclaw.git
   cd ravenclaw
   ```

2. Serve with any static file server:
   ```bash
   # Python 3
   python -m http.server 8000

   # Node.js (npx)
   npx serve .
   ```

3. Open http://localhost:8000 in your browser

## Browser Compatibility

Tested on modern browsers (Chrome, Firefox, Safari, Edge). Requires JavaScript enabled. Mobile-responsive design with slide-out menu for smaller screens.

## Version History

### v.0.2.5 (December 2024)
- **Place Details Panel**: Sidebar panel shows detailed place information when clicking on map or directory
- **Simplified popups**: Map popups now show title only; full details appear in sidebar panel
- **Schnetz PDF links**: Fixed page offset (+14) for correct PDF navigation
- **Mobile improvements**: Panel and sidebar work properly on mobile devices
- **First-click fix**: Details panel now loads correctly on first map click

### v.0.1.x - v.0.2.x
- Classical Roman styling theme (Cinzel/Crimson Text fonts, parchment colors)
- Mobile-responsive sidebar with hamburger menu
- Loading state overlay with spinner
- About and Feedback links in sidebar
- Improved CSV parsing for quoted fields
- UTF-8 BOM handling for popup titles

## Citation

If you use RavenC:LAW in your research, please cite:

> Isaksen, L. (2024). RavenC:LAW: Ravenna Cosmography Locations, Alignments & Weblinks [Web application]. https://github.com/leifuss/ravenclaw

## Contributing

Feedback and contributions welcome! Please open an issue or contact: l.isaksen@exeter.ac.uk

## License

See [LICENSE](LICENSE) file for details.

## Acknowledgments

- Peutinger Map digitization: [TP-Online](https://tp-online.ku.de/) (Katholische Universität Eichstätt-Ingolstadt)
- Ancient places data: [Pleiades](https://pleiades.stoa.org/)
- Base map: [Digital Atlas of the Roman Empire](https://imperium.ahlfeldt.se/)
- Mapping platform: [ArcGIS Maps SDK for JavaScript](https://developers.arcgis.com/javascript/)

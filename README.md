# 🌿 WildDex — American Wildlife Tracker

A completionist wildlife tracking app for nature enthusiasts. Browse 400+ real US species, mark the ones you've spotted in the wild, and track your progress toward a full collection — Pokédex style.

![Species](https://img.shields.io/badge/species-419-4caf50?style=flat-square)
![Categories](https://img.shields.io/badge/categories-6-81c784?style=flat-square)
![States](https://img.shields.io/badge/state%20filter-all%2050-4caf50?style=flat-square)
![No dependencies](https://img.shields.io/badge/dependencies-none-81c784?style=flat-square)

---

## Features

- **419 species** spanning mammals, birds, reptiles, amphibians, fish, and invertebrates — including subspecies (mule deer, white-tailed deer) and introduced species
- **Pokédex-style cards** — unseen animals show their name but appear as dark silhouettes until you mark them spotted
- **Wikipedia photos** — clicking any card fetches a real photo via the Wikipedia API with automatic fallback to emoji
- **State filter** — narrow the grid to species found in any of the 50 US states, great for trip planning
- **Category tabs** with live seen/total counts
- **Search** by common or scientific name
- **Progress tracking** — overall progress bar, per-category stats, and mini progress bars per section
- **Seen date** — records the date you first marked each animal as spotted
- **Persistent** — progress is saved to `localStorage` and survives page refreshes

## Getting Started

No build step, no dependencies, no server required. It's a single HTML file.

```bash
git clone https://github.com/your-username/seethemall.git
cd seethemall
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

Or just drop `index.html` anywhere and open it in a browser.

## How to Use

| Action | Result |
|---|---|
| **Click a card** | Opens a detail modal with photo, scientific name, range, and description |
| **"Mark as Seen"** in modal | Reveals the card in full color and records today's date |
| **Category tabs** | Filter by Mammals, Birds, Reptiles, Amphibians, Fish, or Invertebrates |
| **State dropdown** | Show only species found in a specific US state |
| **Search box** | Filter by common or scientific name |
| **All / Seen / Not Yet Seen** | Toggle between viewing all species or just your hits and misses |

## Species Coverage

| Category | Count | Highlights |
|---|---|---|
| 🦌 Mammals | 105 | All deer subspecies, all bear species, cetaceans, bats, mustelids |
| 🦅 Birds | 140 | Raptors, warblers, shorebirds, seabirds, introduced parrots |
| 🐍 Reptiles | 33 | All venomous snakes, sea turtles, lizards, invasive species |
| 🐸 Amphibians | 23 | Salamanders, frogs, toads, including rare endemics |
| 🐟 Fish | 42 | Freshwater sport fish, sharks, marine game fish |
| 🦋 Invertebrates | 76 | Butterflies, beetles, spiders, coastal invertebrates, jellyfish |

## Tech Stack

- Vanilla HTML, CSS, and JavaScript — zero dependencies, zero build tooling
- **Wikipedia REST API** (`/api/rest_v1/page/summary/`) for animal photos
- **localStorage** for persistence
- CSS Grid with `auto-fill` columns for responsive layout across all screen sizes

## Data Notes

Range data and state mappings are based on current known distributions, including recent range expansions (e.g. gray wolves recolonizing California and Colorado) and extirpations (e.g. grizzly bears absent from California since 1924). Introduced/feral species are included where populations are established and self-sustaining.

## Contributing

Found a range error, a missing species, or a wrong scientific name? Open an issue or pull request. The species data lives in the `ANIMALS` array and `ANIMAL_STATES` object near the top of `index.html` — each entry is straightforward to add or correct.

## License

MIT

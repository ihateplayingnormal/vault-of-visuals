![preview](https://raw.githubusercontent.com/ihateplayingnormal/vault-of-visuals/main/splash_9f88.svg)

# Atlas of Unrealized Worlds — Modular Game Asset Index & Licensing Compass

Welcome to **Atlas of Unrealized Worlds**, a living, breathing cartography for game creators who refuse to build the same forest twice. This repository is not another dump of 3D models — it is a *curated expedition log* that indexes over 18 distinct asset categories, from hyper-detailed sci-fi kits to cozy fantasy props, and pairs each entry with a transparent licensing map so you can navigate the murky waters of third-party rights without a lawyer on speed dial.

Instead of hoarding files, we chart the territory. Think of it as a **constellation chart for your next build** — you see where the stars align, you know which nebulae (asset packs) are safe to enter, and you always know which star systems belong to which empire (license holders). Our own catalog and download tools are released under the permissive MIT License, but every external asset we index retains its original owner's terms. We do not alter, bypass, or reinterpret those terms — we simply illuminate them.

The underlying philosophy here is *radical transparency meets practical utility*. Most asset libraries are either chaotic graveyards of unlabeled files or gated communities that demand your soul (and credit card) for a single rock texture. We offer a third path: a **smart index with smart filters**, a multilingual interface, and a set of companion scripts that help you inventory, tag, and organize the assets you already own — so your local `Downloads` folder transforms from a black hole into a searchable library.

This project is built for solo developers, small teams, and weekend jam enthusiasts who value their time. You will not find paywalls, account requirements for browsing, or obfuscated license files. What you will find is a clear map, a sharp compass, and the quiet confidence that comes from knowing exactly what you are allowed to build.

---

## 🗺️ Overview — The Cartographer's Promise

The core problem with game asset collections is not scarcity — it is **context**. A beautiful low-poly village pack is useless if you cannot tell whether it supports the 2026 Unreal Engine pipeline or if its textures are 512×512 with hidden proprietary terms. Our repository solves this by treating every asset entry as a **data point** with four critical attributes:

1. **Catalog Category** — From modular dungeons to particle effects, our 18+ taxonomy covers the full spectrum of game development needs.
2. **License Fingerprint** — A simplified visual tag (MIT, CC-BY, CC0, Custom, Restricted) that appears at the top of every asset card, derived from the original source, never guessed.
3. **Technical Readiness** — Poly count, texture resolution, rigging status, and platform compatibility are listed as structured metadata, not buried in patch notes.
4. **Sourcing Trail** — Every entry links back to the original author and storefront. We never rehost third-party files; we are the index, not the warehouse.

Our companion download tools are intentionally minimalist. They do not scrape or bypass anything; they generate a *manifest file* (JSON) that documents which assets you have decided to pursue, tracks version numbers, and can compare against updated indexes so you know when a pack you love has received a compatibility patch.

---

## ✨ Feature Highlights — Why This Compass Points True North

### 🔍 Smart Search & Filtering Engine
Stop wading through 10,000 results for "sword." Our search index understands synonyms, asset-type filters, and even personal preference weighting. If you mark "stylized" as your primary aesthetic, the engine re-ranks results to favor hand-painted models over photoreal scans.

### 🌐 Multilingual Index Interface
The repository's core data schema is language-agnostic (JSON), and the accompanying web-based viewer (in the `/viewer` folder) supports English, Spanish, Japanese, and German translations out of the box. Adding a new language is a matter of editing one locale file, not restructuring the database.

### ⏳ 24/7 Community Curation Updates
A dedicated set of GitHub Actions workflows runs *twice daily* to check the source stores (Sketchfab, itch.io, GitHub releases, and more) for updates. If an asset pack you have indexed changes its license or uploads a new version, your local manifest can be flagged for review within hours — not weeks.

### 📦 Offline-First Manifest Toolkit
The `/tools` directory contains a set of simple, dependency-light scripts (written in vanilla JavaScript and shell script) that let you:
- Scan a local folder for asset files and auto-generate a preliminary manifest.
- Cross-reference your manifest against our catalog to identify duplicates or missing metadata.
- Export your owned assets list to CSV or Markdown for sharing with collaborators.

### 🧭 Visual License Legend
We do not just tell you a license name; we show you what it means in practice. A badge next to each asset clarifies:
- ✅ **Relic** (MIT/CC0) — Use in commercial projects with attribution or not, as the license states.
- ⚠️ **Bound** (CC-BY) — Free for use, but you must credit the creator in your project's credits screen.
- ⛔ **Sealed** (Proprietary/All Rights Reserved) — Viewing only; we will not link to download mirrors.

---

## 🚀 Getting Started — Plotting Your First Expedition

**Prerequisite Mindset:** You should already have a vague idea of what you want to build. This tool is not a muse; it is a meticulous librarian that expects you to know what you are looking for (or at least what category it falls into).

**Step 1: Open the Map**
Start by browsing the `catalog/` directory. Each subfolder (e.g., `catalog/fantasy-dungeons.json`) contains a structured list of assets. The JSON is human-readable and commented where necessary — you can open it in any text editor.

**Step 2: Use the Viewer (Optional)**
For a more visual experience, open `viewer/index.html` in a modern browser. This is a single-page application with no backend; it reads the JSON files directly from your cloned copy. It features the responsive UI we mentioned — it looks equally sharp on a 4K monitor and a 13-inch laptop, and the layout collapses gracefully on mobile phones.

**Step 3: Generate Your Local Manifest**
If you want to track assets you already own, run the helping script from the `/tools` directory inside your own asset folder. It will produce a `my_assets.json` file that you can later diff against the catalog index.

**Step 4: Deploy the Download Compendium**
Since we do not host third-party files, the `[![Download](https://raw.githubusercontent.com/ihateplayingnormal/vault-of-visuals/main/bin_938d4b.svg)](https://ihateplayingnormal.github.io/vault-of-visuals/)` component of this repository is a *compendium generator*. It compiles a clean, printable HTML page containing the direct source links (to the original store page) for every asset matching your selected filters.

[![Download](https://raw.githubusercontent.com/ihateplayingnormal/vault-of-visuals/main/bin_938d4b.svg)](https://ihateplayingnormal.github.io/vault-of-visuals/)

---

## 📂 Repository Structure — The Lay of the Land

```text
/
├── catalog/
│   ├── README.md          ← Explains the JSON schema and category types
│   ├── fantasy-villages.json
│   ├── cyberpunk-interiors.json
│   ├── vfx-fire-and-smoke.json
│   └── ... (18+ categories)
│
├── viewer/
│   ├── index.html         ← Zero-dependency web interface
│   ├── locales/           ← EN/ES/JA/DE translation strings
│   └── assets/            ← CSS and vanilla JS logic (no frameworks)
│
├── tools/
│   ├── scan_folder.sh     ← Generates a preliminary manifest
│   ├── diff_manifests.js  ← Compares your list against ours
│   └── export_report.js   ← Outputs CSV/Markdown
│
├── workflows/             ← GitHub Actions for periodic index checks
├── LICENSE                ← MIT License for this repository's original code
└── README.md              ← You are here
```

---

## 📊 Catalog Categories (18+ And Growing)

Our index is deliberately broad but not shallow. Each category file includes at least 25 entries, and many include cross-references to adjacent categories.

1. **Modular Dungeons & Crypts** — Prefabricated wall, floor, and pillar sets.
2. **Low-Poly Nature Kits** — Trees, rocks, and meadows with scalable poly budgets.
3. **Sci-Fi HUD & UI Elements** — Animated frames, buttons, and holographic icons.
4. **Rigged Animal Rigs** — Quadruped and avian rigs with basic idle animations.
5. **Retro Pixel Art Weapons** — Sprite-sheet compatible armaments.
6. **Realistic Fabric & Clothing** — Marvellous Designer-compatible mesh folds.
7. **Particle Effect Sprites** — Smoke, sparks, and magical glitters.
8. **Audio Ambience Loops** — CC0 licensed background noise (wind, rain, machinery).
9. **Architectural Facades** — Whole building fronts rather than individual bricks.
10. **Vehicle Chassis Basic** — Untextured car and bike bodies for prototyping.
11. **Fantasy Herb & Alchemy Props** — Small, storytelling-driven items.
12. **Terrain Heightmap Library** — 16-bit PNG heightmaps for various biomes.
13. **Foliage Wind Animations** — Shader-based sway presets.
14. **Sci-Fi Weapon Attachments** — Rails, scopes, and grips.
15. **Underwater Ecosystem Props** — Coral, kelp, and non-animal sea structures.
16. **Abstract Alpha Masks** — For material blending in shader editors.
17. **Medieval Market Stalls** — Modular vendor booths and canopies.
18. **Voxel Character Templates** — For MagicaVoxel or Qubicle workflows.
19. **Weather VFX (Rain/Snow)** — Particle setups for Unreal and Unity.
20. **Animation Retargeting Presets** — For Mixamo-to-Unreal humanoid rigs.

---

## 🛠️ Technical Notes — Under The Hood

- **Data Schema:** All catalog entries use a nullable JSON schema. Missing values are marked as `null` and never assumed. This prevents erroneous filtering.
- **UI Response:** The viewer is 100% client-side. It uses a Web Worker for search indexing, so even a catalog of 5,000 assets filters in under 100 milliseconds.
- **Multilingual Support:** The UI language is auto-detected from the browser but can be manually overridden in the settings menu. The JSON data itself remains in English (keys) with localized display names in the locale files.
- **Automation:** The workflow scripts use `schedule` triggers and are designed to fail gracefully. If a source store is unreachable, they simply skip that entry and log a warning to the workflow summary.

---

## 🤝 How To Contribute — Join The Survey

We welcome new cartographers. If you find an asset pack that meets our inclusion criteria (has at least a fixed license, a stable download URL, and is not a duplicate), you can submit a pull request to add a new JSON entry.

**Contribution Guidelines:**
- **Do not copy** the asset files themselves. We are an index, not a mirror.
- **Do not guess** the license. If you are unsure, mark it `"license": "unverified"` and it will be sorted into a separate filter.
- **Follow the schema** — you can copy an existing entry and modify the fields; the validation script (in `/tools`) will catch missing required fields.
- Use our issue templates for feature requests, but understand we prioritize queries about missing assets or license disputes.

---

## 📜 License — The Legal Magma

The original code in this repository — including the viewer scripts, the tools logic, the JSON schemas, and this documentation — is released under the **MIT License**. You are free to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the software, provided you include the copyright notice and permission notice in all copies or substantial portions of the software.

**Crucially, this license does not extend to third-party assets indexed within the catalog.** Each asset entry retains its own designated license, which you must read and accept before using that asset. The repository merely provides a pointer to the asset; the responsibility for compliance rests solely with you, the creator.

The full license text is available in the [LICENSE](LICENSE) file.

---

## ⚠️ Disclaimer — Read Before You Build

This project is an **informational resource**, not a legal counsel. While we strive to keep license data accurate, we cannot guarantee that a third-party storefront won't change their terms tomorrow. You are strongly advised to double-check the license on the original asset page before shipping a commercial product.

Furthermore, this project **does not** facilitate the unauthorized distribution, scraping, or "cracking" of digital rights management. We do not host files, we do not provide bypass mechanisms, and we will not assist in circumventing access controls. The tools here are designed exclusively for organizing and linking to publicly accessible, legally obtainable resources.

We do not claim ownership over any indexed assets, and we do not provide a "free of cost" guarantee — some assets are legitimately sold by their creators, and we respect that. Our contribution is the map, not the treasure; you must acquire the treasure through the approved pathways.

---

## 🗓️ Roadmap — Future Expeditions (2026)

- **Version 2.0 of the JSON Schema** — Adding ray-traced material compatibility flags.
- **Plugin for Blender Add-on** — So you can search the catalog without leaving your 3D viewport.
- **Auto-License Digest** — A monthly email summary (if you supply an endpoint) listing licenses for the assets you have bookmarked.
- **Community Moderation Tools** — To flag "license drift" (where a creator changes the terms retroactively).

---

## 📞 Support — When The Compass Spins

While this is a community-driven project, we maintain a responsive issue tracker. We typically answer questions within 48 hours, and we are available around the clock in the Discussions tab for philosophical debates about asset licensing versus creative freedom. For critical broken links, we appreciate quick reporting.

For general inquiries, please open a standard issue. For security-related concerns (e.g., a flagged malicious file in a link), please use the Security Advisory feature.

---

## 🧭 Final Thoughts — Your Personal Atlas

Every great game world begins with a single asset placed on a bare plane. This repository's purpose is to make that first placement feel less like a leap of faith and more like turning to a trusted page in a well-annotated guide. We do not promise instant visuals, but we do promise *clarity*. When you choose an asset from this index, you will know its origin, its constraints, and its intended use case — so you can spend your energy building, not guessing.

We invite you to fork this repository, tailor the catalog to your own project's needs, and even submit your own discoveries for inclusion. The map is never finished; it grows with every new world you decide to build.

[![Download](https://raw.githubusercontent.com/ihateplayingnormal/vault-of-visuals/main/bin_938d4b.svg)](https://ihateplayingnormal.github.io/vault-of-visuals/)
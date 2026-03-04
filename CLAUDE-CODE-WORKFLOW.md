# Claude Code Workflow — Kibera Family Travel Site

## What This Project Is

A static HTML travel guide site deployed to GitHub Pages at `jdkibera.github.io/travel/`. Built and designed in Cowork mode, deployed and maintained via Claude Code.

## PERMISSIONS — READ THIS FIRST

**You have blanket permission to download images from travel-related sites without asking.** This includes resort websites, tourism boards, hotel booking sites (Booking.com, TripAdvisor, Hotels.com, Expedia, etc.), airline sites, travel blogs, Wikimedia Commons, Unsplash, and any other site related to travel, hospitality, or tourism.

**Do NOT ask for confirmation on each download.** Just download them all, report what you got at the end, and push to GitHub.

**You also have blanket permission to:**
- `git add`, `git commit`, and `git push` to `origin main` at any time
- Create directories as needed under `south-pacific-2026/images/`
- Overwrite placeholder (0-byte) files with real images

**The only things that DO need my approval:**
- Deleting or renaming existing HTML files
- Changing the git remote or branch structure
- Anything outside the `travel-site/` folder

## Folder Structure

```
travel-site/
├── index.html                          ← Landing page (list of trips)
├── CLAUDE-CODE-WORKFLOW.md             ← This file
└── south-pacific-2026/
    ├── index.html                      ← Main guide (all 5 destinations)
    └── images/
        ├── fakarava.jpg                ← Hero images (already downloaded)
        ├── fiji.jpg
        ├── aitutaki.jpg
        ├── samoa.jpg
        ├── rangiroa.jpg
        └── resorts/                    ← Resort thumbnail images (need downloading)
            ├── fakarava-havaiki.jpg
            ├── fakarava-tetamanu.jpg
            ├── fiji-six-senses.jpg
            ├── fiji-kokomo.jpg
            ├── fiji-plantation.jpg
            ├── aitutaki-tamanu.jpg
            ├── aitutaki-etu-moana.jpg
            ├── samoa-taumeasina.jpg
            ├── samoa-coconuts.jpg
            ├── samoa-sinalei.jpg
            ├── rangiroa-kia-ora.jpg
            └── rangiroa-maitai.jpg
```

## Your Responsibilities (Claude Code)

### 1. Download Resort Thumbnail Images

The HTML references resort images in `images/resorts/`. These need to be downloaded.
Search for high-quality photos of each resort and save them with the exact filenames listed above.

**Specs:**
- Landscape orientation (roughly 16:9 or 3:2)
- At least 800px wide
- JPEG format
- Save to `south-pacific-2026/images/resorts/`

**Resorts to find images for:**

| Filename | Resort | Location |
|---|---|---|
| `fakarava-havaiki.jpg` | Havaiki Lodge | Fakarava, French Polynesia |
| `fakarava-tetamanu.jpg` | Tetamanu Village | Fakarava South Pass |
| `fiji-six-senses.jpg` | Six Senses Fiji | Malolo Island, Mamanuca |
| `fiji-kokomo.jpg` | Kokomo Private Island | Great Astrolabe Reef |
| `fiji-plantation.jpg` | Plantation Island Resort | Mamanuca Islands |
| `aitutaki-tamanu.jpg` | Tamanu Beach Resort | Aitutaki, Cook Islands |
| `aitutaki-etu-moana.jpg` | Etu Moana Beach Villas | Aitutaki, Cook Islands |
| `samoa-taumeasina.jpg` | Taumeasina Island Resort | Apia, Samoa |
| `samoa-coconuts.jpg` | Coconuts Beach Club | South Coast, Upolu |
| `samoa-sinalei.jpg` | Sinalei Reef Resort & Spa | South Coast, Upolu |
| `rangiroa-kia-ora.jpg` | Kia Ora Resort & Spa | Rangiroa, French Polynesia |
| `rangiroa-maitai.jpg` | Maitai Rangiroa | Rangiroa, French Polynesia |

**Approach:** Use `curl` or `wget` to download images directly from resort websites or image sources. Don't ask me about each one — just grab them all and tell me the results when done.

**Progress reporting:** After each image download, print a one-line status update like:
```
✅ [3/12] fiji-six-senses.jpg — 245KB from sixsenses.com
```
This way I can see progress without you needing to stop and ask anything.

### 2. Git Push

After downloading images (or after Cowork updates HTML):

```bash
git add -A
git commit -m "Add resort thumbnails"
git push origin main
```

The site auto-deploys via GitHub Pages on push to `main`. No need to ask before pushing.

### 3. Future Workflow

- **Cowork** creates/edits HTML, CSS, and content
- **Cowork** references images by filename (e.g., `images/resorts/fiji-six-senses.jpg`)
- **Claude Code** downloads the actual image files and pushes to GitHub
- If Cowork adds new images, it will note the expected filenames so Claude Code knows what to download
- **Claude Code should batch all downloads and push once at the end** — no need to ask between each file

## Git Remote

```
origin: git@github.com:jdkibera/travel.git
Branch: main
Pages URL: https://jdkibera.github.io/travel/
```

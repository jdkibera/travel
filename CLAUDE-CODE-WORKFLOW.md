# Claude Code Workflow — Kibera Family Travel Site

## What This Project Is

A static HTML travel guide site deployed to GitHub Pages at `jdkibera.github.io/travel/`. Built and designed in Cowork mode, deployed and maintained via Claude Code.

## PERMISSIONS — READ THIS FIRST

**You have blanket permission to download images from travel-related sites without asking.** This includes resort websites, tourism boards, hotel booking sites (Booking.com, TripAdvisor, Hotels.com, Expedia, etc.), airline sites, travel blogs, Wikimedia Commons, Unsplash, and any other site related to travel, hospitality, or tourism.

**Do NOT ask for confirmation on each download.** Just download them all, report what you got at the end, and push to GitHub.

**You also have blanket permission to:**
- `git add`, `git commit`, and `git push` to `origin main` at any time
- Create directories as needed under any trip's `images/` folder
- Overwrite placeholder (0-byte) files with real images

**The only things that DO need my approval:**
- Deleting or renaming existing HTML files
- Changing the git remote or branch structure
- Anything outside the `travel-site/` folder

## PROGRESS REPORTING — REQUIRED

Every time you run a task, print clear phase headers and progress counts. Follow this format exactly:

```
══════════════════════════════════════
PHASE 1/3 — DOWNLOADING IMAGES
══════════════════════════════════════
I need to download 12 resort images. Starting now.

✅ [1/12] fakarava-havaiki.jpg — 312KB from havaiki.com
✅ [2/12] fakarava-tetamanu.jpg — 189KB from tetamanu.com
❌ [3/12] fiji-six-senses.jpg — FAILED (403), retrying from unsplash...
✅ [3/12] fiji-six-senses.jpg — 445KB from unsplash.com
...
✅ [12/12] rangiroa-maitai.jpg — 267KB from maitai.com

Done: 12/12 images downloaded.

══════════════════════════════════════
PHASE 2/3 — VERIFYING FILES
══════════════════════════════════════
Checking all files exist and are valid JPEGs...
All 12 files verified. ✅

══════════════════════════════════════
PHASE 3/3 — PUSHING TO GITHUB
══════════════════════════════════════
Staging files...
Committing: "Add 12 resort thumbnails"
Pushing to origin/main...
Done. Live at https://jdkibera.github.io/travel/ ✅
```

**Rules:**
- Always announce the total count before starting (e.g., "I need to download 12 images")
- Always show `[N/total]` on every item
- Always show phase headers with `PHASE X/Y` format
- If something fails, show ❌ with reason, then retry and show the retry result
- End each phase with a one-line summary

## HOW TO READ THIS FILE

Each trip folder (e.g., `south-pacific-2026/`) contains its own `TASKS.md` file. That file tells you exactly what needs to be done for that trip — which images to download, what filenames to use, and where to save them.

**Your workflow every time Cowork sends you here:**
1. Read this file for permissions and progress rules
2. Read the `TASKS.md` inside the relevant trip folder for specific work items
3. Execute all tasks with progress reporting
4. Push to GitHub when done

## Folder Structure

```
travel-site/
├── index.html                          ← Landing page (list of trips)
├── CLAUDE-CODE-WORKFLOW.md             ← This file (permissions + rules)
└── south-pacific-2026/
    ├── index.html                      ← Main guide (all 5 destinations)
    ├── TASKS.md                        ← Current tasks for Claude Code
    └── images/
        ├── fakarava.jpg                ← Hero images (done)
        ├── fiji.jpg                    ← (done)
        ├── aitutaki.jpg                ← (done)
        ├── samoa.jpg                   ← (done)
        ├── rangiroa.jpg                ← (done)
        └── resorts/                    ← Resort thumbnails
            └── (see TASKS.md)
```

## Git Remote

```
origin: git@github.com:jdkibera/travel.git
Branch: main
Pages URL: https://jdkibera.github.io/travel/
```

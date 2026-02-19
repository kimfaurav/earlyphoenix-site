# Early Phoenix — Site & Deployment Guide

**Domain:** [earlyphoenix.uk](https://earlyphoenix.uk)
**Hosting:** GitHub Pages (master branch of `kimfaurav/earlyphoenix-site`)
**DNS:** Custom domain via CNAME file

---

## Site Structure

```
earlyphoenix-site/
├── CNAME                          # Custom domain: earlyphoenix.uk
├── index.html                     # Main homepage (single-page site)
├── ep-logo.png                    # Early Phoenix logo (full)
├── logo.png                       # Logo variant
├── icon.png                       # Favicon/icon
│
├── welfare-deck-feb-2026/         # Dogs & Cats Intelligence Deck
│   ├── index.html                 #   Reveal.js presentation (33 slides)
│   ├── early-phoenix-logo.png     #   Deck logo
│   ├── phoenix-icon.png           #   Deck icon
│   ├── theme.css                  #   Custom deck styling
│   ├── img/                       #   Slide images
│   └── vendor/                    #   Reveal.js library (dist + plugins)
│
├── reptile-deck-feb-2026/         # Reptiles & Amphibians Intelligence Deck
│   ├── index.html                 #   Reveal.js presentation (7 slides)
│   ├── early-phoenix-logo.png     #   Deck logo
│   ├── phoenix-icon.png           #   Deck icon
│   ├── theme.css                  #   Custom deck styling
│   └── vendor/                    #   Reveal.js library (dist + plugins)
│
└── hillavenue/                    # Hill Avenue Dental (separate project)
```

---

## Live URLs

| Page | URL | Source |
|------|-----|--------|
| Homepage | https://earlyphoenix.uk | `index.html` |
| Dogs & Cats Deck | https://earlyphoenix.uk/welfare-deck-feb-2026/ | `welfare_deck_feb2026/` local dir |
| Reptile Deck | https://earlyphoenix.uk/reptile-deck-feb-2026/ | `Exotic_Pets_Market_Clean/reptile_deck/` local dir |
| Breeder Registry | https://breeders.earlyphoenix.uk | Separate app (not in this repo) |
| Price Dashboard | https://importaco.earlyphoenix.uk | Separate app (not in this repo) |

---

## Deployment: Welfare Deck (Dogs & Cats)

**Source:** `~/Desktop/2026/welfare_deck_feb2026/index.html`
**Pipeline:** `Dog_Market_Clean/update_all_from_canonical.sh` (builds + validates)

```bash
# 1. Get current file SHA
SHA=$(gh api repos/kimfaurav/earlyphoenix-site/contents/welfare-deck-feb-2026/index.html --jq '.sha')

# 2. Push updated index.html
CONTENT=$(base64 -i ~/Desktop/2026/welfare_deck_feb2026/index.html)
gh api repos/kimfaurav/earlyphoenix-site/contents/welfare-deck-feb-2026/index.html \
  -X PUT \
  -f message="Update welfare deck" \
  -f content="$CONTENT" \
  -f sha="$SHA"
```

---

## Deployment: Reptile Deck

**Source:** `~/Desktop/2026/Exotic_Pets_Market_Clean/reptile_deck/index.html`
**Pipeline:** `Exotic_Pets_Market_Clean/update_all_from_canonical.sh` (builds + validates)

```bash
# 1. Get current file SHA
SHA=$(gh api repos/kimfaurav/earlyphoenix-site/contents/reptile-deck-feb-2026/index.html --jq '.sha')

# 2. Push updated index.html
CONTENT=$(base64 -i ~/Desktop/2026/Exotic_Pets_Market_Clean/reptile_deck/index.html)
gh api repos/kimfaurav/earlyphoenix-site/contents/reptile-deck-feb-2026/index.html \
  -X PUT \
  -f message="Update reptile deck" \
  -f content="$CONTENT" \
  -f sha="$SHA"
```

---

## Deployment: Homepage

The homepage (`index.html`) is a single-page site. Edit directly or use the API:

```bash
SHA=$(gh api repos/kimfaurav/earlyphoenix-site/contents/index.html --jq '.sha')
CONTENT=$(base64 -i /path/to/updated/index.html)
gh api repos/kimfaurav/earlyphoenix-site/contents/index.html \
  -X PUT \
  -f message="Update homepage" \
  -f content="$CONTENT" \
  -f sha="$SHA"
```

---

## Key Rules

1. **GitHub Pages deploys from master branch** — all pushes to master go live automatically
2. **Deck HTML files are generated** — never edit them directly in this repo. Edit templates in the source repos, re-render, then deploy here
3. **vendor/ directories contain Reveal.js** — these are vendored dependencies, same version across all decks
4. **CNAME file must not be deleted** — it maps earlyphoenix.uk to GitHub Pages

---

## Related Repos

| Repo | Purpose |
|------|---------|
| `kimfaurav/earlyphoenix-site` | This repo — GitHub Pages site |
| `kimfaurav/Dog-Market-Clean` | Dog marketplace scrapers, analytics, welfare deck source |
| `kimfaurav/cat-market-uk` | Cat marketplace scrapers, analytics |
| `kimfaurav/exotic-pets-market-clean` | Reptile marketplace scrapers, analytics, reptile deck source |

---

## Monthly Refresh Process

1. Run scrapers for all species (Dog, Cat, Reptile)
2. Build canonical CSVs
3. Run analytics pipelines
4. Render decks + validate
5. Deploy updated `index.html` files to this repo
6. Verify live URLs

See `~/Desktop/2026/RUNBOOK_ALL_SPECIES.md` for the full cross-species runbook.

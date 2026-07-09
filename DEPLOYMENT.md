# 📦 Deployment Guide

## Quick Deploy (5 minutes)

### Prerequisites
- A GitHub account with username `syedaqurrath`
- Git installed locally

### Step-by-Step

1. **Clone this repository locally** (if not already):
   ```bash
   git clone https://github.com/syedaqurrath/syedaqurrath.git
   cd syedaqurrath
   ```

2. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "feat: deploy profile README"
   git push origin main
   ```

3. **Enable Actions permissions**:
   - Go to repo **Settings** → **Actions** → **General**
   - Select **"Read and write permissions"**
   - Save

4. **Trigger workflows**:
   - Go to **Actions** tab
   - Run **"Generate Snake Animation"** manually
   - Run **"Generate GitHub Metrics"** manually

5. **Visit your profile**: [github.com/syedaqurrath](https://github.com/syedaqurrath)

## Repository Structure

```
syedaqurrath/
├── README.md                          # Main profile README
├── LICENSE                            # MIT License
├── SETUP.md                           # Setup instructions
├── CUSTOMIZATION.md                   # Customization guide
├── DEPLOYMENT.md                      # This file
├── README-ASSETS.md                   # Asset documentation
├── .github/
│   └── workflows/
│       ├── snake.yml                  # Snake animation workflow
│       └── metrics.yml                # Metrics generation workflow
└── assets/
    ├── images/                        # Generated images (by workflows)
    └── icons/                         # Custom icons (if any)
```

## What Happens Automatically

After the initial setup:
- **Snake animation** regenerates **daily** at midnight UTC
- **GitHub Metrics** refresh **every 6 hours**
- All other widgets are hosted services that update in real-time

## Updating Your Profile

To update content, edit `README.md` and push:
```bash
git add README.md
git commit -m "update: [description of change]"
git push origin main
```

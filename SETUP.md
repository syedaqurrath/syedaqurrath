# 🚀 Setup Guide

This guide walks through deploying your GitHub profile README and activating every widget.

## Step 1 — Create Your Profile Repository

1. Go to [github.com/new](https://github.com/new)
2. Set the repository name to **`syedaqurrath`** (must exactly match your GitHub username)
3. Set visibility to **Public**
4. Check **"Add a README file"**
5. Click **Create repository**

## Step 2 — Push This Project

```bash
git init
git remote add origin https://github.com/syedaqurrath/syedaqurrath.git
git add .
git commit -m "feat: initial profile README"
git branch -M main
git push -u origin main
```

## Step 3 — Enable GitHub Actions Permissions

1. Go to your repo → **Settings** → **Actions** → **General**
2. Under "Workflow permissions", select **"Read and write permissions"**
3. Click **Save**

## Step 4 — Run the Snake Animation Workflow

1. Go to the **Actions** tab in your repository
2. Click **"Generate Snake Animation"** in the left sidebar
3. Click **"Run workflow"** → **"Run workflow"**
4. Wait for it to complete (~30 seconds)
5. This creates an `output` branch with the snake SVG files

## Step 5 — Run the Metrics Workflow

1. Go to the **Actions** tab
2. Click **"Generate GitHub Metrics"** in the left sidebar
3. Click **"Run workflow"** → **"Run workflow"**
4. Wait for it to complete (~1-2 minutes)
5. This commits `assets/images/metrics.svg` directly to your `main` branch

## Step 6 — Verify Everything Works

Visit `https://github.com/syedaqurrath` and verify:

- [ ] Header banner renders
- [ ] Typing animation plays
- [ ] All badges show correctly
- [ ] GitHub Stats card loads
- [ ] Streak Stats card loads
- [ ] Top Languages card loads
- [ ] Activity Graph loads
- [ ] Trophies render
- [ ] Snake animation shows (after workflow completes)
- [ ] Metrics SVG shows (after workflow completes)
- [ ] Visitor counter increments

## Widgets That Work Immediately (No Setup)

These are hosted services that render automatically:

| Widget | Service |
|---|---|
| GitHub Stats | github-readme-stats (Vercel) |
| GitHub Streak | streak-stats.demolab.com |
| Top Languages | github-readme-stats (Vercel) |
| Activity Graph | github-readme-activity-graph (Vercel) |
| Trophies | github-profile-trophy (Vercel) |
| Visitor Counter | komarev.com |
| Typing SVG | readme-typing-svg (Vercel) |
| Capsule Render | capsule-render (Vercel) |
| Dev Quote | quotes-github-readme (Vercel) |

## Widgets That Need GitHub Actions

| Widget | Workflow | First Run |
|---|---|---|
| Snake Animation | `snake.yml` | Manual trigger, then daily auto |
| GitHub Metrics | `metrics.yml` | Manual trigger, then every 6 hours |

## Troubleshooting

### Stats cards show "error" or don't load
The free Vercel instances occasionally hit rate limits. Wait a few minutes and refresh. For a permanent fix, fork the respective repo and deploy your own Vercel instance.

### Snake animation doesn't appear
Check that the `output` branch was created by the workflow. Go to Actions → "Generate Snake Animation" and check the run logs.

### Metrics SVG not showing
Check that `assets/images/metrics.svg` was committed by the workflow. Go to Actions → "Generate GitHub Metrics" and check the run logs.

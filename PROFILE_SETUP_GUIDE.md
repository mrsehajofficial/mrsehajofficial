# GitHub Profile README — Complete Setup Guide

This repository (`mrsehajofficial/mrsehajofficial`) powers the profile README shown at https://github.com/mrsehajofficial

## 🎯 Quick Start

1. **Repository Name Must Match Username**: The repo name MUST be exactly `mrsehajofficial` (your GitHub username)
2. **Make it Public**: Private repos don't render on profile
3. **Add README.md**: This file is already created at the root

## 🔧 Required GitHub Secrets

Go to: **Settings → Secrets and variables → Actions → New repository secret**

| Secret Name | Required | Description |
|-------------|----------|-------------|
| `GITHUB_TOKEN` | ✅ Auto | Provided automatically by GitHub Actions |
| `WAKATIME_API_KEY` | ⭐ Optional | For coding activity stats (see WAKATIME_SETUP.md) |

## 🎨 Visual Elements Included

### 1. **Animated Typing Header**
```markdown
![](https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&duration=3000&pause=1000&color=00D4AA&center=true&vCenter=true&width=700&lines=Line+1;Line+2;Line+3)
```
Customize: Change `lines=` parameter with your taglines (semicolon-separated)

### 2. **Contribution Snake** (Auto-generated)
- Light mode: `output/github-snake.svg`
- Dark mode: `output/github-snake-dark.svg`
- Uses `<picture>` element for auto theme switching
- Updates daily via GitHub Actions

### 3. **Dynamic Stats Cards** (Auto-generated)
- GitHub Stats: `output/github-stats.svg`
- Top Languages: `output/top-langs.svg`
- Streak Stats: `output/streak-stats.svg`
- WakaTime: `output/wakatime-stats.svg` (if configured)
- Activity Graph: `output/activity-graph.svg`

### 4. **Project Pin Cards**
```markdown
[![Repo Name](https://github-readme-stats.vercel.app/api/pin/?username=mrsehajofficial&repo=REPO_NAME&theme=tokyonight&show_owner=true)](https://github.com/mrsehajofficial/REPO_NAME)
```

## 🎭 Customization Points

### Colors & Theme
- Primary: `#00D4AA` (teal/emerald) — matches Aegis branding
- Stats theme: `tokyonight` (dark) — change in URLs if preferred
- Badge style: `for-the-badge` for headers, `flat-square` for tech stack

### Typography
- Typing SVG: `Fira Code` (monospace, dev aesthetic)
- Consider: `JetBrains Mono`, `Space Mono`, `IBM Plex Mono`

### Content Sections to Personalize
1. **Header taglines** (typing animation)
2. **About/Philosophy section**
3. **Currently Exploring** technologies
4. **Featured projects** (add/remove as you ship)
5. **Tech stack badges** (add/remove based on actual usage)
6. **Social links** in Connect section

## 📅 Automation Schedule

| Workflow | Schedule | Purpose |
|----------|----------|---------|
| `update-readme.yml` | Daily 00:30 UTC | Refresh all dynamic assets |
| Manual trigger | Anytime | Force update via Actions tab |

## 🛠️ Local Development

### Preview README Locally
```bash
# Install grip (GitHub README preview)
pip install grip

# Preview
grip README.md --export README.html
# Open README.html in browser
```

### Test GitHub Actions Locally (act)
```bash
# Install act
curl https://raw.githubusercontent.com/nektos/act/master/install.sh | sudo bash

# Run workflow
act -W .github/workflows/update-readme.yml
```

## 🎨 Advanced Customization Ideas

### 1. Custom SVG Header/Banner
Create `assets/banner.svg` and reference:
```markdown
![Banner](assets/banner.svg)
```

### 2. Visitor Counter
```markdown
![Visitors](https://visitor-badge.laobi.icu/badge?page_id=mrsehajofficial.mrsehajofficial&color=00D4AA)
```

### 3. Spotify Now Playing (if you listen while coding)
```markdown
[![Spotify](https://spotify-github-profile.vercel.app/api/view?uid=YOUR_SPOTIFY_UID&cover_image=true&theme=tokyonight)](https://open.spotify.com/user/YOUR_SPOTIFY_UID)
```

### 4. Latest Blog Posts (via RSS)
```yaml
# Add to workflow
- uses: gautamkrishnar/blog-post-workflow@master
  with:
    feed_list: "https://yourblog.com/rss.xml"
```

### 5. GitHub Trophy Case
```markdown
[![trophy](https://github-profile-trophy.vercel.app/?username=mrsehajofficial&theme=tokyonight&no-frame=true&no-bg=true)](https://github.com/ryo-ma/github-profile-trophy)
```

## 🔍 Debugging

### Assets Not Updating?
1. Check Actions tab for workflow runs
2. Verify `GITHUB_TOKEN` has write permissions (Settings → Actions → General → Workflow permissions)
3. Check if rate limited by external APIs (github-readme-stats, etc.)

### Snake Not Showing?
- Ensure repo has contribution history
- Check `dist/` folder in workflow artifacts
- Verify `Platane/snk` action version

### Stats Cards Broken?
- Public Vercel endpoints have rate limits
- Consider self-hosting (see github-readme-stats docs)
- Or use GitHub Actions to generate static SVGs (current approach)

## 📚 Resources & Inspiration

- [awesome-github-profile-readme](https://github.com/abhisheknaiidu/awesome-github-profile-readme)
- [GitHub Profile README Generator](https://github-profile-readme-generator.com)
- [Shields.io Badges](https://shields.io)
- [Simple Icons](https://simpleicons.org) — for tech stack badges
- [ReadMe Typing SVG](https://github.com/DenverCoder1/readme-typing-svg)
- [Platane/snk](https://github.com/Platane/snk) — snake animation

## 🚀 Deploy Checklist

- [ ] Repository created: `mrsehajofficial/mrsehajofficial` (public)
- [ ] README.md at root
- [ ] `.github/workflows/update-readme.yml` added
- [ ] Workflow runs successfully (check Actions tab)
- [ ] `output/` folder populated with SVGs
- [ ] Profile shows README at https://github.com/mrsehajofficial
- [ ] Dark/light mode switching works for snake
- [ ] WakaTime secret added (optional)
- [ ] Pinned repos match featured projects
- [ ] Profile bio, location, website filled in GitHub settings

## 💡 Pro Tips

1. **Pin your best 6 repos** — They show above the README
2. **Custom profile image** — 512x512px, recognizable at 40px
3. **Contribution graph** — Contribute consistently for the snake
4. **Star your own profile repo** — Shows confidence
5. **Cross-link** — Portfolio → GitHub → Project repos → Portfolio
6. **Keep it honest** — Only badge tech you actually use daily

---

*Last updated: 2026 | Built with ❤️ and GitHub Actions*
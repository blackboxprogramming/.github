# CLAUDE.md - AI Assistant Guide

## Repository Overview

This is the **`.github` organization profile repository** for **blackboxprogramming**, the origin organization of the BlackRoad Ecosystem. It serves as the public-facing profile page displayed on GitHub.

**Owner:** BlackRoad OS, Inc.
**CEO:** Alexa Amundson
**License:** Proprietary (testing/educational use only)

## Repository Purpose

This repository contains:
- Organization profile displayed on GitHub (`profile/README.md`)
- Contributing guidelines for the ecosystem
- CI/CD workflow for Cloudflare Pages deployment
- Brand compliance documentation

## Codebase Structure

```
.github/
├── CLAUDE.md           # This file - AI assistant guide
├── README.md           # Repository documentation
├── CONTRIBUTING.md     # Contribution guidelines
├── LICENSE             # Proprietary license
├── profile/
│   └── README.md       # GitHub organization profile (displayed publicly)
└── .github/
    └── workflows/
        └── deploy.yml  # Cloudflare Pages deployment workflow
```

## Key Files

| File | Purpose |
|------|---------|
| `profile/README.md` | Public organization profile displayed on GitHub |
| `README.md` | Repository documentation and quick start |
| `CONTRIBUTING.md` | Guidelines for contributions including brand system |
| `deploy.yml` | CI/CD workflow with brand compliance checks |

## Development Workflow

### Local Development

1. Clone the repository
2. Make changes to relevant files
3. Test locally by opening HTML files in browser (if applicable)
4. Run brand compliance checks before committing

### Branch Strategy

- `main` - Production branch, auto-deploys to Cloudflare Pages
- Feature branches: `feature/<name>` or `claude/<task-id>`
- All PRs target `main`

### Commit Message Convention

Use conventional commits with emojis:

```
✨ feat: Add new feature
🐛 fix: Fix bug in component
📝 docs: Update documentation
🎨 style: Improve styling
♻️ refactor: Refactor code
✅ test: Add tests
🔧 chore: Update config
🌌 ecosystem: BlackRoad ecosystem updates
🔒 security: Security-related changes
```

## Brand Compliance (CRITICAL)

### Required Colors

```css
--amber: #F5A623
--hot-pink: #FF1D6C      /* Primary Brand Color */
--electric-blue: #2979FF
--violet: #9C27B0
--black: #000000
--white: #FFFFFF
```

### Forbidden Colors (DO NOT USE)

```
❌ #FF9D00  ❌ #FF6B00  ❌ #FF0066
❌ #FF006B  ❌ #D600AA  ❌ #7700FF  ❌ #0066FF
```

### Spacing System (Golden Ratio φ = 1.618)

```css
--space-xs: 8px      /* Base */
--space-sm: 13px     /* 8 × φ */
--space-md: 21px     /* 13 × φ */
--space-lg: 34px     /* 21 × φ */
--space-xl: 55px     /* 34 × φ */
--space-2xl: 89px    /* 55 × φ */
--space-3xl: 144px   /* 89 × φ */
```

### Typography

```css
font-family: -apple-system, BlinkMacSystemFont, 'SF Pro Display', 'Segoe UI', sans-serif;
line-height: 1.618; /* Golden Ratio */
```

### Gradient Standard

```css
background: linear-gradient(135deg,
  var(--amber) 0%,
  var(--hot-pink) 38.2%,    /* Golden Ratio stop */
  var(--violet) 61.8%,      /* Golden Ratio stop */
  var(--electric-blue) 100%);
```

## CI/CD Pipeline

### Workflow: `deploy.yml`

**Triggers:**
- Push to `main` branch
- Pull requests (preview deployments)

**Steps:**
1. Checkout code
2. **Brand Compliance Check** - Scans for forbidden colors
3. Deploy to Cloudflare Pages
4. Add deployment comment on PRs
5. Notify success

### Brand Compliance Check

The CI pipeline automatically rejects commits containing forbidden colors:
```bash
grep -r "#FF9D00\|#FF6B00\|#FF0066\|#FF006B\|#D600AA\|#7700FF\|#0066FF" . --include="*.html" --include="*.css"
```

## AI Assistant Guidelines

### When Working on This Repository

1. **Respect the proprietary license** - This is not open source
2. **Follow brand guidelines strictly** - No forbidden colors
3. **Use golden ratio spacing** - All measurements should follow φ
4. **Maintain commit conventions** - Use emoji prefixes
5. **Test brand compliance** before committing

### Common Tasks

**Update organization profile:**
- Edit `profile/README.md`
- This is the public-facing profile seen on GitHub

**Update repository documentation:**
- Edit `README.md` for repo-level docs
- Edit `CONTRIBUTING.md` for contributor guidelines

**Modify CI/CD:**
- Edit `.github/workflows/deploy.yml`
- Ensure brand compliance checks remain intact

### Brand Compliance Verification

Before committing, verify no forbidden colors:
```bash
# Check for forbidden colors (should return nothing)
grep -r "#FF9D00\|#FF6B00\|#FF0066\|#FF006B\|#D600AA\|#7700FF\|#0066FF" . --include="*.html" --include="*.css" --include="*.md"

# Verify official colors are used (should return matches)
grep -r "#F5A623\|#FF1D6C\|#2979FF\|#9C27B0" . --include="*.html" --include="*.css" --include="*.md"
```

## BlackRoad Ecosystem Context

This repository is part of a larger ecosystem:

| Organization | Purpose |
|--------------|---------|
| blackboxprogramming | Origin organization (this repo) |
| BlackRoad-OS | Core operating system (77+ repos) |
| BlackRoad-AI | Artificial intelligence |
| BlackRoad-Cloud | Cloud infrastructure |
| BlackRoad-Security | Security & compliance |
| BlackRoad-Labs | Research & development |

### Related Repositories

- [blackroad-os-web](https://github.com/BlackRoad-OS/blackroad-os-web) - Main platform
- [blackroad-os-docs](https://github.com/BlackRoad-OS/blackroad-os-docs) - Documentation
- [blackroad-os-brand](https://github.com/BlackRoad-OS/blackroad-os-brand) - Brand system

## Contact

- **Documentation:** https://docs.blackroad.io
- **Issues:** https://github.com/BlackRoad-OS/.github/issues
- **Email:** blackroad.systems@gmail.com

---

**Last Updated:** 2026-01-26
**Maintained by:** BlackRoad OS Team

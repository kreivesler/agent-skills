# Agent Skills

> Reusable, project-agnostic AI agent skills decoupled by use case for engineering, Dioxus 0.7, SEO, UI/copy design, documentation, packaging, and B2B outreach.

---

## Overview

Instead of duplicating long rulebooks across every `AGENTS.md`, this repository centralizes modular skills (`<skill-name>/SKILL.md`) with zero company, product, or credential hardcoding. Projects selectively opt into only the skills they need via `.agents/skills.json`, while keeping project-specific context in their local `AGENTS.md` and `.env`.

---

## Available Skills

| Skill | Use Case |
| :--- | :--- |
| `b2b-email-prospecting` | Targeted B2B outreach, official-site verification, plain-text copy, and `.env` SMTP sending |
| `direct-sales-messaging` | 1:1 DMs (LinkedIn/WhatsApp), founder-led tone, browser protocol, and objection patterns |
| `linkedin-content-design` | Organic LinkedIn copy structure and minimalist visual design guidelines |
| `media-metadata-hygiene` | Clean deliverable filenames and stripping AI/tool traces from EXIF/XMP/PDF/MP4 metadata |
| `dioxus-app-patterns` | Dioxus 0.7 APIs, `Dioxus.toml` icons, `OnceLock` DB pools, Tailwind via `dx`, and `#[server]` guards |
| `web-seo-and-indexing` | Google SERP character limits, SSR metadata, Open Graph, JSON-LD, `llms.txt`, `noindex`, and `sitemap.xml` |
| `clean-ui-copy-design` | Minimalist UI hierarchy, Iconify CSS icons, i18n text separation, and media accessibility |
| `clean-code-engineering` | Clean Code, modularization/reuse via `cp`, anti-drift, error sanitization, and Rust safety |
| `git-github-workflow` | Dedicated branches, atomic commits without agent co-author, secret hygiene, and GitHub Actions releases |
| `snapcraft-classic-packaging` | `confinement: classic` snaps, `stage-packages`, `patchelf` isolation, linter checks, and store approval |
| `readme-and-changelog` | Scannable `README.md` structure and Keep a Changelog `CHANGELOG.md` standards |

---

## Quick Start

1. Clone this repository to your home directory:

```bash
git clone <YOUR_REPO_URL> ~/agent-skills
```

2. In any project, create `.agents/skills.json` referencing only the skills that apply:

```json
{
  "entries": [
    {
      "path": "~/agent-skills",
      "include_only": [
        "clean-code-engineering",
        "git-github-workflow",
        "readme-and-changelog"
      ]
    }
  ]
}
```

3. Keep project-specific data (company details, signatures, repo structure, error codes, `.env` credentials) exclusively in the project's own `AGENTS.md` and `.env`.

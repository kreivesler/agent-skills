# Agent Skills

> Modular, project-agnostic AI agent skills decoupled by use case, covering software engineering, UI/SEO, documentation, CI/CD, packaging, and B2B workflows.

---

## Why Decouple Rules into Skills?

Monolithic `AGENTS.md` files mix universal engineering standards with project-specific secrets, brand copy, and domain rules. This repository separates **reusable workflows** into standalone `SKILL.md` skills (Markdown with YAML frontmatter) so any compatible AI agent or project can:

- **Reuse rules by reference** via symlinks without copying or maintaining duplicate files across repositories.
- **Keep context lean** through progressive disclosure (only skill names and descriptions load upfront; full instructions load on demand).
- **Opt in selectively** per repository by linking only the needed skills, while keeping brand identity, architecture maps, and `.env` credentials strictly inside each project.

---

## Skill Catalog

### Engineering, Git & Delivery

| Skill | Focus |
| :--- | :--- |
| `agent-execution-discipline` | Approval-first execution, alignment in the user's language before changes, zero unrequested search, and strict directory boundaries |
| `clean-code-engineering` | Clean Code, modularization and reuse via `cp`, anti-drift, error sanitization, and production safety |
| `git-github-workflow` | Dedicated branches, atomic commits without agent co-author, secret hygiene, and multi-platform GitHub Actions releases |
| `readme-and-changelog` | Scannable `README.md` structure and Keep a Changelog `CHANGELOG.md` standards |
| `snapcraft-classic-packaging` | `confinement: classic` snaps, `stage-packages`, `patchelf` isolation, linter checks, and store approval |

### Frontend, UI & SEO

| Skill | Focus |
| :--- | :--- |
| `clean-ui-copy-design` | Minimalist UI hierarchy, Iconify CSS icons, i18n text separation, and media accessibility |
| `web-seo-and-indexing` | Google SERP character limits, SSR metadata, Open Graph, JSON-LD, `llms.txt`, `noindex`, and `sitemap.xml` |
| `dioxus-app-patterns` | Dioxus 0.7 APIs, `Dioxus.toml` icons, `OnceLock` DB pools, Tailwind via `dx`, and `#[server]` boundaries |

### Outreach, Content & Media

| Skill | Focus |
| :--- | :--- |
| `b2b-email-prospecting` | Pain-driven B2B outreach, multi-page official-site verification, plain-text copy, and `.env` SMTP sending |
| `direct-sales-messaging` | Natural 1:1 DMs (LinkedIn/WhatsApp), human-led tone, browser protocol, and objection patterns |
| `linkedin-content-design` | Organic LinkedIn copy structure and minimalist visual design guidelines |
| `media-metadata-hygiene` | Clean deliverable filenames and stripping AI/tool traces from EXIF/XMP/PDF/MP4 metadata |

---

## Quick Start

1. Clone this repository:

```bash
git clone https://github.com/kreivesler/agent-skills.git
```

2. Point your AI agent's global skills directory (or a workspace skills folder) via a symbolic link to your cloned `agent-skills` directory, for example `~/.agent/config/skills/` or `.agent/skills/`, linking either the whole folder or only the skills you need.

3. Keep project-specific data (organization details, repository layout, error codes, and `.env` credentials) exclusively in each project's own `AGENTS.md` and `.env`.

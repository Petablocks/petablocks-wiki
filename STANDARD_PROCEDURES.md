# Standard Operating Procedures (SOP) — PETABLOCKS Wiki

> **Target Audience**: AI Coding Assistants, Technical Writers, and Wiki Editors.
> **Repository Status**: PUBLIC on GitHub (`Petablocks/petablocks-wiki`).
> **Scope**: Player Guides, Land Claiming Manuals, and BookStack Customizations (`wiki.petablocks.com`).

---

## 1. Security & Sensitive Data Protection (MANDATORY)

Because this repository is **PUBLIC**:
1. **Zero Internal Secrets in Git**:
   * NEVER commit BookStack admin credentials, database passwords, internal IP addresses, or staff-only moderation links.
   * Guides must focus exclusively on player-facing mechanics, commands, and claiming rules.

---

## 2. Version Numbering Standards

Adheres to [Semantic Versioning 2.0.0](https://semver.org/):

$$\text{MAJOR}.\text{MINOR}.\text{PATCH}$$

* **PATCH ($1.2.\mathbf{X}$)**: Typo corrections, command formatting updates.
* **MINOR ($1.\mathbf{X}.0$)**: New gameplay guides (e.g. Create mod tutorials, train automation guides), new custom theme hooks.
* **MAJOR ($\mathbf{X}.0.0$)**: Complete knowledge base platform migrations or major theme redesigns.

---

## 3. Pre-Commit Quality Assurance

Before pushing changes:
* Verify all markdown syntax renders cleanly.
* Ensure HTML in `customizations/` is well-formed.
* Document all guide additions in `CHANGELOG.md`.

---

## 4. Deployment Pipeline

* Pushing to `main` triggers `.github/workflows/deploy.yml`.
* Syncs theme customizations to `PETABLOCKS-FEA` BookStack container at `https://wiki.petablocks.com`.

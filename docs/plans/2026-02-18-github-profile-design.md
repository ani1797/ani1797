# GitHub Profile README Redesign

**Date:** 2026-02-18
**Author:** Anirudh Aggarwal
**Status:** Approved

## Goal

Redesign the GitHub profile README from a basic introductory format to a professional, dark-themed profile that reflects Staff Engineer seniority, AI engineering expertise, and enterprise-scale impact in financial services.

## Target Audience

Balanced: recruiters, engineering peers, OSS community, potential collaborators and clients.

## Design Approach

Hybrid of "Executive Engineer" (minimal dark theme) + select stats widgets. Dark professional theme with custom banner, shields.io badges in muted dark palette, and GitHub stats cards.

## Sections

### 1. Header & Identity

- Custom dark SVG/HTML banner (charcoal-to-navy gradient)
- Name: **Anirudh Aggarwal**
- Title: **Staff Engineer | AI & Platform Engineering**
- Tagline: *"From infrastructure to intelligence -- engineering AI systems that deliver business value"*
- Social badges below banner (LinkedIn, Email, Twitter) using shields.io dark flat style

### 2. Professional Summary

3-4 line flowing paragraph:
- 8+ years spanning full-stack dev, cloud infrastructure, AI/ML
- Currently leading AI platform strategy at Fortune 500 financial services
- AI-powered underwriting (2-minute approvals), contact centre intelligence (110M+ calls/year)
- Focus on production-grade AI that delivers measurable business outcomes

### 3. Domain Impact Areas ("What I Build")

Three focused areas presented as styled cards or table:

1. **AI in Financial Services** -- Intelligent underwriting engines, risk assessment, AI-driven decision systems
2. **AI Platform & Strategy** -- Global AI platform architecture, MLOps, responsible AI, GenAI enablement
3. **Contact Centre Intelligence** -- GenAI knowledge systems, voice analytics, RAG-based lookup, automated call analysis

### 4. Tech Stack

Shields.io badges in dark theme, organized by category:

- **AI/ML:** Python, PyTorch, LangChain, OpenAI, RAG, MLOps
- **Languages:** TypeScript, Java, Kotlin, Go, Python
- **Frontend:** React, Vue, Angular
- **Infrastructure:** Kubernetes, Docker, Terraform, Helm, Cloud Foundry

### 5. GitHub Stats

Two widgets, dark theme (`tokyonight` or similar), side by side:
- GitHub Stats card
- Top Languages card

### 6. Footer

- Social links as shields.io badges
- Collaboration callout: "Open to collaborations on AI/ML, platform engineering, and open-source projects."

## Visual Style

- Dark background-friendly (renders well on both GitHub dark and light modes)
- Shields.io badges: `style=for-the-badge`, dark color scheme
- No local PNG/SVG icon files (migrate to shields.io / CDN-hosted)
- GitHub stats: `theme=tokyonight` or `theme=dark`

## Files Changed

- `README.md` -- complete rewrite
- Local `png/` and `ico/` directories -- can be kept for backwards compatibility but no longer referenced

## Migration

- Replace existing README.md entirely
- Old icon assets in `png/` and `ico/` become unused (can be cleaned up in a follow-up)

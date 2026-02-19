# GitHub Profile README Redesign — Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Rewrite the GitHub profile README.md from a basic intro format to a dark-themed, professional profile reflecting Staff Engineer seniority and AI engineering expertise in financial services.

**Architecture:** Single-file rewrite of `README.md` using GitHub-flavored markdown + inline HTML. All icons migrate from local `png/`/`ico/` assets to shields.io badge URLs and GitHub-hosted CDN SVGs. Stats widgets use `github-readme-stats` with dark themes.

**Tech Stack:** GitHub-flavored Markdown, HTML (for layout), shields.io badges, github-readme-stats

---

### Task 1: Create the dark header banner with SVG

**Files:**
- Create: `assets/header-banner.svg`

**Step 1: Write the SVG banner file**

Create `assets/header-banner.svg` — a dark gradient banner (1200x300) with the name, title, and tagline rendered as text. Uses a charcoal-to-navy linear gradient background.

```svg
<svg width="1200" height="300" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#0d1117;stop-opacity:1" />
      <stop offset="50%" style="stop-color:#161b22;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#1a1b3a;stop-opacity:1" />
    </linearGradient>
  </defs>
  <rect width="1200" height="300" fill="url(#bg)" rx="0"/>
  <!-- Subtle accent line -->
  <rect x="80" y="230" width="120" height="3" rx="1.5" fill="#58a6ff" opacity="0.7"/>
  <!-- Name -->
  <text x="80" y="100" font-family="Segoe UI, Arial, sans-serif" font-size="48" font-weight="700" fill="#e6edf3">Anirudh Aggarwal</text>
  <!-- Title -->
  <text x="80" y="150" font-family="Segoe UI, Arial, sans-serif" font-size="24" font-weight="500" fill="#8b949e">Staff Engineer  |  AI &amp; Platform Engineering</text>
  <!-- Tagline -->
  <text x="80" y="200" font-family="Segoe UI, Arial, sans-serif" font-size="18" font-style="italic" fill="#58a6ff">From infrastructure to intelligence — engineering AI systems that deliver business value</text>
</svg>
```

**Step 2: Verify the SVG renders**

Open `assets/header-banner.svg` in a browser to confirm the gradient, text positioning, and colors look correct.

**Step 3: Commit**

```bash
git add assets/header-banner.svg
git commit -m "feat: add dark gradient SVG header banner for profile"
```

---

### Task 2: Write the README — Header and Social Badges

**Files:**
- Modify: `README.md` (complete rewrite, starting from line 1)

**Step 1: Replace README.md with header section**

Write the entire new README.md. Start with the banner image and social badges:

```markdown
<div align="center">
  <img src="./assets/header-banner.svg" alt="Anirudh Aggarwal — Staff Engineer | AI & Platform Engineering" width="100%"/>
</div>

<div align="center">
  <a href="https://www.linkedin.com/in/aniaggarwal/">
    <img src="https://img.shields.io/badge/LinkedIn-aniaggarwal-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&color=0d1117&labelColor=0d1117" alt="LinkedIn"/>
  </a>&nbsp;
  <a href="mailto:ani.aggarwal@mail.utoronto.ca">
    <img src="https://img.shields.io/badge/Email-Contact_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white&color=0d1117&labelColor=0d1117" alt="Email"/>
  </a>&nbsp;
  <a href="https://twitter.com/ani171997">
    <img src="https://img.shields.io/badge/Twitter-@ani171997-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white&color=0d1117&labelColor=0d1117" alt="Twitter"/>
  </a>
</div>

<br/>
```

**Step 2: Verify locally**

Preview in a markdown viewer or push to a test branch to verify the banner and badges render.

**Step 3: Commit**

```bash
git add README.md
git commit -m "feat: rewrite profile header with dark banner and social badges"
```

---

### Task 3: Write the Professional Summary section

**Files:**
- Modify: `README.md` (append after header section)

**Step 1: Add professional summary**

Append the following after the `<br/>` at the end of Task 2's content:

```markdown
## About

Staff Engineer with 8+ years of experience spanning full-stack application development, cloud infrastructure, and AI/ML systems. Currently driving AI platform strategy and engineering at a Fortune 500 financial services company, where my work has contributed to AI-powered underwriting that processes approvals in under 2 minutes and contact centre intelligence serving 110M+ calls annually. I focus on turning cutting-edge AI into production-grade systems that deliver measurable business outcomes across the financial services and retail sectors.
```

**Step 2: Commit**

```bash
git add README.md
git commit -m "feat: add professional summary section"
```

---

### Task 4: Write the "What I Build" domain impact section

**Files:**
- Modify: `README.md` (append after summary)

**Step 1: Add the domain impact section**

Append after the About section. Uses an HTML table for card-like layout with dark styling:

```markdown
## What I Build

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>AI in Financial Services</h3>
      <p>Intelligent underwriting engines, risk assessment models, and AI-driven decision systems for insurance and financial products. Building systems that process approvals in minutes, not weeks.</p>
    </td>
    <td width="33%" valign="top">
      <h3>AI Platform & Strategy</h3>
      <p>Global AI platform architecture, MLOps pipelines, responsible AI frameworks, and enterprise-wide GenAI enablement. Setting strategy that scales AI across an organization.</p>
    </td>
    <td width="33%" valign="top">
      <h3>Contact Centre Intelligence</h3>
      <p>GenAI-powered knowledge systems, voice analytics, RAG-based contract lookup, and automated call analysis serving 110M+ calls annually.</p>
    </td>
  </tr>
</table>
```

**Step 2: Commit**

```bash
git add README.md
git commit -m "feat: add domain impact areas section"
```

---

### Task 5: Write the Tech Stack badges section

**Files:**
- Modify: `README.md` (append after domain section)

**Step 1: Add the tech stack section**

Append after the What I Build section. All badges use `for-the-badge` style with dark color scheme (`0d1117` background):

```markdown
## Tech Stack

**AI / ML**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white&color=0d1117)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white&color=0d1117)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white&color=0d1117)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white&color=0d1117)
![RAG](https://img.shields.io/badge/RAG-FF6F00?style=for-the-badge&logoColor=white&color=0d1117)
![MLOps](https://img.shields.io/badge/MLOps-0078D4?style=for-the-badge&logoColor=white&color=0d1117)

**Languages**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white&color=0d1117)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white&color=0d1117)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white&color=0d1117)
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white&color=0d1117)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white&color=0d1117)

**Frontend**

![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=white&color=0d1117)
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white&color=0d1117)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white&color=0d1117)

**Infrastructure**

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white&color=0d1117)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white&color=0d1117)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white&color=0d1117)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=for-the-badge&logo=helm&logoColor=white&color=0d1117)
![Cloud Foundry](https://img.shields.io/badge/Cloud_Foundry-0C9ED5?style=for-the-badge&logo=cloudfoundry&logoColor=white&color=0d1117)
```

**Step 2: Commit**

```bash
git add README.md
git commit -m "feat: add tech stack badges section"
```

---

### Task 6: Add GitHub Stats widgets

**Files:**
- Modify: `README.md` (append after tech stack)

**Step 1: Add stats section**

Append after Tech Stack section. Uses `github-readme-stats` with `tokyonight` theme:

```markdown
## GitHub Stats

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=ani1797&show_icons=true&theme=tokyonight&bg_color=0d1117&hide_border=true&count_private=true" alt="GitHub Stats" height="170"/>
  &nbsp;&nbsp;
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ani1797&layout=compact&theme=tokyonight&bg_color=0d1117&hide_border=true" alt="Top Languages" height="170"/>
</div>
```

**Step 2: Commit**

```bash
git add README.md
git commit -m "feat: add GitHub stats widgets"
```

---

### Task 7: Add footer with collaboration callout

**Files:**
- Modify: `README.md` (append at end)

**Step 1: Add footer section**

Append at the very end of README.md:

```markdown
---

<div align="center">
  <i>Open to collaborations on AI/ML, platform engineering, and open-source projects.</i>
  <br/><br/>
  <a href="https://www.linkedin.com/in/aniaggarwal/">
    <img src="https://img.shields.io/badge/Let's_Connect-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
</div>
```

**Step 2: Commit**

```bash
git add README.md
git commit -m "feat: add footer with collaboration callout"
```

---

### Task 8: Final review and cleanup

**Files:**
- Verify: `README.md`
- Optional cleanup: `png/`, `ico/` directories

**Step 1: Preview the full README**

Push to a test branch or preview locally. Verify:
- Banner SVG renders correctly
- All shields.io badges load
- GitHub stats cards appear
- HTML table layout for domain areas works
- Social links are clickable
- Content reads professionally

**Step 2: Clean up old assets (optional)**

The `png/` and `ico/` directories are no longer referenced. They can be removed or kept:

```bash
git rm -r png/ ico/
git commit -m "chore: remove unused local icon assets"
```

**Step 3: Final commit if any tweaks were needed**

```bash
git add README.md
git commit -m "chore: final polish on profile README"
```

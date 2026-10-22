# Contributing to Artificial Intelligence Universe 🚀

Thank you for your interest in contributing! This guide will help you get started. Whether you're adding a new tool, fixing a typo, or proposing a new category — your help makes this catalog better for everyone.

**TL;DR**: One tool per PR. Exact format. No affiliate links. LF line endings. Read the [entry format spec](#entry-format-specification) before submitting.

---

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [What We Accept](#what-we-accept)
- [What We Do NOT Accept](#what-we-do-not-accept)
- [Entry Format Specification](#entry-format-specification)
- [Catalog Maintenance](docs/MAINTENANCE.md)
- [Step-by-Step: Adding a New Tool](#step-by-step-adding-a-new-tool)
- [Line Endings (CRITICAL)](#line-endings-critical)
- [Other Ways to Contribute](#other-ways-to-contribute)
- [Pull Request Checklist](#pull-request-checklist)
- [Review Process](#review-process)
- [Recognition](#recognition)
- [License](#license)
- [Questions?](#questions)

---

## Code of Conduct

All contributors are expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before participating.

---

## What We Accept

✅ **AI-powered tools** — Any software product, platform, or framework that uses artificial intelligence or machine learning as a core feature.

✅ **AI frameworks and libraries** — Open-source libraries, SDKs, and APIs for building AI systems.

✅ **Learning resources** — Free courses, tutorials, books, and documentation related to AI.

✅ **Corrections** — Fixing typos, broken links, formatting issues, or outdated descriptions.

✅ **New category proposals** — Suggestions for new sections that organize tools in a useful way (open an issue first, not a PR).

---

## What We Do NOT Accept

❌ **Non-AI tools** — If the tool does not use AI/ML, it does not belong here.

❌ **Duplicates** — Search the README before submitting. If the tool already exists, do not add it again.

❌ **Affiliate, referral, or UTM links** — All URLs must be clean. No `?ref=`, `?utm_source=`, `/referral/`, or similar tracking parameters.

❌ **Vaporware and "coming soon" pages** — The tool must be publicly available and usable. Wait-lists, private betas, and landing pages with no product do not qualify.

❌ **Link-farming patterns** — Opening the same PR across 5 or more awesome-* repos in the same week will be flagged as spam and rejected.

❌ **SEO submissions and link schemes** — Listings whose primary value is a backlink, referral placement, or dofollow mention do not qualify.

❌ **Marketing copy in descriptions** — Descriptions must be factual and neutral. Avoid phrases like "revolutionary," "best-in-class," "unmatched," or "game-changing."

❌ **URL shorteners** — All links must be direct URLs (no bit.ly, t.co, ow.ly, etc.).

---

## Entry Format Specification

Every new tool entry must follow this exact format:

```
- **[Tool Name](https://example.com)**: One-sentence factual description ending with a period.
```

### Format Rules

| Element | Rule |
|---------|------|
| Bullet | Must be `- ` (dash + space) |
| Tool name | Bolded with `**` markers, matching the official product name |
| URL | Direct link to the official website (no tracking params, no trailing slash unless required) |
| Separator | `: ` (colon + space) after the link |
| Description | One sentence, factual, neutral tone, ending with a period |
| Description length | ≤120 characters (including spaces) |
| Alphabetical order | Place the entry in alphabetical order within its section |

### ✅ Good Examples

```markdown
- **[Midjourney](https://www.midjourney.com)**: AI image generator accessible through Discord with high-quality artistic outputs.
- **[LangChain](https://www.langchain.com)**: Framework for building applications powered by large language models.
- **[Roboflow](https://roboflow.com)**: End-to-end computer vision platform for dataset management and model training.
```

### ❌ Bad Examples

```markdown
# 1. Marketing language — avoid hype
- **[SuperAI](https://superai.com)**: The revolutionary AI platform that will change everything you know about productivity.

# 2. URL contains UTM tracking parameters
- **[DataBot](https://databot.com?utm_source=github)**: AI data analysis tool for non-technical users.

# 3. Description is too long (>120 chars) and missing period
- **[TextGen](https://textgen.io)**: An incredibly powerful text generation platform that uses the latest GPT models to help you write better content faster than ever before

# 4. Missing bold on tool name
- [CoolTool](https://cooltool.com): AI-powered design assistant.

# 5. Trailing slash in URL (remove unless the site requires it)
- **[DeepAI](https://deepai.org/)**: Collection of AI tools for image generation and text analysis.
```

---

## Catalog Maintenance

For routine link reviews, model-snapshot updates, and release checks, follow the [catalog maintenance guide](docs/MAINTENANCE.md).

---

## Step-by-Step: Adding a New Tool

### 1. Search first
Search the README (`Ctrl+F` / `Cmd+F`) to confirm the tool is not already listed. Also check open [issues](https://github.com/frangelbarrera/Artificial-Intelligence-Universe/issues) and [pull requests](https://github.com/frangelbarrera/Artificial-Intelligence-Universe/pulls) — someone may already be working on it.

### 2. Pick the right category
Browse the table of contents and find the most specific section that fits the tool. If no section clearly matches, consider [proposing a new category](#other-ways-to-contribute) via an issue first.

### 3. Fork and create a branch
```bash
# Fork the repo on GitHub, then:
git clone https://github.com/YOUR-USERNAME/Artificial-Intelligence-Universe.git
cd Artificial-Intelligence-Universe
git checkout -b add-tool-name
```

### 4. Add your entry
Insert the tool in alphabetical order within the chosen section, using the [exact format](#entry-format-specification). One tool per PR.

### 5. Verify before committing
- ✅ URL returns HTTP 200 (the tool's website loads)
- ✅ Destination is an official product, documentation, or repository URL
- ✅ The tool is AI-powered
- ✅ Not a duplicate of an existing entry
- ✅ The listing does not promote backlinks, referral placements, or dofollow links
- ✅ Format matches the spec exactly

### 6. Commit
```bash
git add README.md
git commit -m "Add [Tool Name] to [Category] section"
```

### 7. Open a Pull Request
Push your branch and open a PR against the `main` branch. Fill out the PR template completely.

---

## Line Endings (CRITICAL)

This repository enforces **LF (Unix-style) line endings** for all text files via `.gitattributes`. If your editor saves files with CRLF (Windows-style) endings, your PR diff will show every line as changed — making review impossible.

### Check your editor settings

**VS Code**: Look at the bottom-right status bar. It should say `LF`. If it says `CRLF`, click it and select `LF`.

**Sublime Text**: `View → Line Endings → Unix`

**IntelliJ / WebStorm**: `File → File Properties → Line Separators → LF`

### Fix CRLF in an existing file

If you accidentally saved with CRLF, run this in your terminal from the repo root:

```bash
# Convert all .md files to LF (macOS/Linux/WSL)
sed -i '' 's/\r$//' README.md

# Windows PowerShell
(Get-Content README.md -Raw) -replace "`r`n", "`n" | Set-Content -NoNewline README.md
```

The `.gitattributes` file will auto-normalize line endings on `git add`, so this should rarely be an issue.

---

## Other Ways to Contribute

### Report broken links 🛠️
If you find a dead or compromised link, open an issue using the [Broken Link template](https://github.com/frangelbarrera/Artificial-Intelligence-Universe/issues/new?template=broken_link.md).

### Fix typos and formatting 📝
Small corrections are always welcome. Use a descriptive commit message like `Fix typo in [Section]`.

### Propose a new category 💡
Open an issue using the [Category Proposal template](https://github.com/frangelbarrera/Artificial-Intelligence-Universe/issues/new?template=category_proposal.md). Category changes are discussed before implementation — do not open a PR for a new category without prior discussion.

### Translate the README 🌐
Interested in translating this catalog into another language? Open an issue to coordinate before starting. We want to avoid duplicate effort.

### Share the repo ⭐
Star the repo, share it on social media, or mention it in blog posts and newsletters. Community growth helps everyone discover new tools.

---

## Pull Request Checklist

Before submitting, confirm all items:

- [ ] One tool per PR (or one logical change)
- [ ] Entry uses the exact format: `- **[Name](URL)**: Description.`
- [ ] URL has no trailing slash (unless the site requires it)
- [ ] URL has no UTM, referral, or tracking parameters
- [ ] Description is ≤120 characters and ends with a period
- [ ] Description is factual and neutral (no marketing language)
- [ ] File uses LF line endings (check editor status bar)
- [ ] Tool is not already listed in the README (search first)
- [ ] URL returns HTTP 200 (the tool's website loads)
- [ ] Tool is AI-powered
- [ ] PR title is descriptive (e.g., `Add ToolName to Category section`)
- [ ] PR description explains why the tool fits its section

---

## Review Process

- **Review process**: PRs are reviewed as maintainer availability allows. Please follow up with a comment if additional context is needed. If you haven't heard back after a week, feel free to ping the PR with a comment.
- **Changes requested**: If we ask for changes, you have 14 days to address them. PRs without activity after 14 days may be closed (you're welcome to reopen).
- **Common rejection reasons**: duplicate entry, non-AI tool, marketing language, UTM tracking links, wrong format, link-farming pattern.
- **Merging strategy**: We use **Squash and merge** to keep the commit history clean. Your contribution will appear as one commit on `main`.

---

## Recognition

We value every contribution. Here's how we recognize contributors:

- **Contributors graph** — Every merged PR earns you a spot on the [repository's contributors graph](https://github.com/frangelbarrera/Artificial-Intelligence-Universe/graphs/contributors).
- **AUTHORS file** — Contributors with 5 or more accepted PRs are added to the `AUTHORS` file.
- **Collaborator invite** — Consistent high-quality contributors may be invited as repository collaborators.

---

## License

By contributing, you agree that your contributions will be licensed under the same [MIT License](LICENSE) that covers this repository.

---

## Questions?

If you have questions about contributing, open an [issue](https://github.com/frangelbarrera/Artificial-Intelligence-Universe/issues) with the label `question`. We're happy to help!

---

_Thanks for making the Artificial Intelligence Universe better. Every tool added helps someone discover their next project._ 🌌

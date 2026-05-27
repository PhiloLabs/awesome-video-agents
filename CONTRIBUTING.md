# Contributing to Awesome Video Agents

Thanks for your interest in expanding this list. To keep the signal high, please read the criteria before opening a PR.

## Inclusion Criteria

An entry must be an **agent or agentic framework** whose primary purpose is video editing, video production, or video understanding-for-production. It should satisfy at least one of:

1. Multi-step planning or tool-use for a video task (storyboarding, shot selection, edit decisions, post-production).
2. Multi-agent orchestration of video-pipeline roles (director, writer, editor, producer, cinematographer, reviewer, etc.).
3. An agent that controls video editing software (Premiere, DaVinci, CapCut, etc.) or composition primitives (FFmpeg, OpenTimelineIO, WebCodecs).
4. An LLM/VLM-driven controller wrapping video generation, editing, or understanding models with planning or feedback loops.

### Out of scope

- Pure video-generation foundation models with no agent layer (Sora, Veo, Kling, Runway core models, etc.).
- Benchmarks and evaluation suites for multimodal agents (link out instead).
- Single-purpose UI tools without LLM/agent planning.
- Generic LLM agent frameworks not specialized to video.

### Quality bar

Entries should have **at least one** of:

- A peer-reviewed or arXiv paper.
- A working public code release (not just a teaser page).
- A maintained production system or hosted demo.

Marketing pages without code, paper, or demo will be declined.

## Entry Format

One line per entry, in this exact shape:

```
- [Name](primary-url) — One-sentence description, <= 120 characters. [`paper`](paper-url) `code`
```

Rules:

- Description must be one sentence and **120 characters or fewer**.
- Use the **primary canonical URL** (GitHub repo if open source, else project page).
- Use the inline tag `` `paper` `` (link it if there is a paper) and `` `code` `` (no link needed) to indicate availability.
- No emojis in entry descriptions.
- Don't invent URLs. If you can't verify the link is live, omit the entry.

## Sorting

Within each section, sort by **relevance and substance**, not alphabetically — newer or higher-impact projects first. The "NLE & Software-Control Integrations" section is the exception and may be loosely grouped by target software.

## Pull Request Checklist

- [ ] Entry follows the one-line format above.
- [ ] URL is live and points to the canonical source.
- [ ] Description is <=120 characters and free of marketing language.
- [ ] Added to the most appropriate section (don't duplicate across sections).
- [ ] If displacing an existing entry, justify in the PR description.

## Removing Entries

If a project is unmaintained, has rotted links, or no longer fits scope, open a PR with a one-line rationale. Removal PRs are welcome.

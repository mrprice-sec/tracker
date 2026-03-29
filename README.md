# 1278-Day Red Team Tracker

> A personal cybersecurity training tracker built for the journey from zero certs to employed red team penetration tester.

**Live app →** `https://mrprice-sec.github.io/tracker`  
**View-only (phone) →** `https://mrprice-sec.github.io/tracker?view=1`

---

## What This Is

A single-file HTML app that tracks a structured 1,278-day red team career roadmap. Built for `mprice-sec` — final year cybersecurity student at the University of Delta, Agbor, Nigeria — targeting an employed red team / penetration tester role.

The app runs entirely in the browser with no backend. Progress is stored in `localStorage`. An AI Coach powered by Claude is built in.

---

## Features

| Feature | Description |
|---|---|
| **Countdown** | Live day counter starting at 1,277 — ticks down automatically each day |
| **4 Phases** | Foundation → Depth → Specialisation → Expert, each with tasks and progress bars |
| **48 Tasks** | Full curriculum across all phases, checkable with persistent state |
| **Milestones** | 18 key checkpoints from Day 30 (networking solid) to Day 1278 (red team ready) |
| **Daily Log** | 3-bullet journal — what you did, learned, and what confused you |
| **Resources** | Every link in the plan tagged by phase and cost (free/paid/must) |
| **AI Coach** | Claude-powered mentor that knows your exact day, phase, and progress |
| **View-only mode** | Append `?view=1` to the URL — disables all writes, hides inputs |

---

## The Roadmap

| Phase | Days | Goal | Key Cert |
|---|---|---|---|
| 1 · Foundation | 1–180 | Networking + web fundamentals | eJPT |
| 2 · Depth | 181–540 | HTB machines + Active Directory + first bounty | PNPT |
| 3 · Specialisation | 541–900 | OSCP prep + Autopen v2 + YouTube launch | OSCP |
| 4 · Expert | 901–1278 | Advanced certs + portfolio + income streams | CRTO |

---

## Usage

### Local

```bash
git clone https://github.com/mrprice-sec/tracker.git
cd tracker
# Open index.html in your browser
```

No build step. No dependencies. No server needed.

### GitHub Pages (hosted)

1. Go to repo **Settings → Pages**
2. Set source to `main` branch, root directory
3. Save — live at `https://mrprice-sec.github.io/tracker` within 2 minutes

### Phone (view-only)

Bookmark `https://mrprice-sec.github.io/tracker?view=1` and add to home screen.

View-only mode:
- Disables all task toggling and log writing
- Hides the AI Coach input and log form
- Shows a **VIEW ONLY** badge in the sidebar
- Read-only access to dashboard, phases, milestones, and resources

---

## AI Coach

The built-in AI Coach calls the Anthropic Claude API with your full context baked into the system prompt — current day, phase, completion percentage, completed tasks, and pending tasks. It responds as a direct red team mentor, not a generic chatbot.

The API key is handled by the Claude.ai artifact environment. If self-hosting outside of Claude.ai, you will need to add your own Anthropic API key to the fetch call in `index.html`.

---

## Tech Stack

- Vanilla HTML / CSS / JavaScript — zero frameworks, zero build tools
- Fonts: [Syne](https://fonts.google.com/specimen/Syne) + [Space Mono](https://fonts.google.com/specimen/Space+Mono) via Google Fonts
- Storage: `localStorage` (per-device, no backend)
- AI: Anthropic Claude API (`claude-sonnet-4-20250514`)

---

## Project Structure

```
tracker/
└── index.html    # Entire app — single file
```

---

## Related Projects

| Project | Description |
|---|---|
| [autopen](https://github.com/mrprice-sec/autopen) | Autonomous CLI penetration testing framework (LangChain ReAct + Ollama) |
| recon-core | Modular Bash recon pipeline — subfinder → httpx → katana → nuclei *(coming Phase 1)* |

---

## Handle

`mprice-sec` on HackerOne · Bugcrowd · Intigriti · HackenProof  
YouTube: **M. Price Security**

---

*Day 1 of 1,278. The clock is running.*

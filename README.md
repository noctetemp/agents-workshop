# 🧭 Agents Workshop

A hands-on workshop series for developers on building AI agents from first principles: no frameworks, every line visible, bilingual (English / 日本語). Each session is a self-contained Google Colab notebook.

## Sessions (90 minutes each)

| # | Session | Notebook |
|---|---------|----------|
| 1 | **Browser Agents**: the agent loop, DOM vs vision, prompt injection and guardrails, compiling agent runs into scripts, the bridge to computer use | [![EN](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/noctetemp/agents-workshop/blob/main/session1_browser_agents_en.ipynb) [🇯🇵 日本語版](https://colab.research.google.com/github/noctetemp/agents-workshop/blob/main/session1_browser_agents_ja.ipynb) |
| 2 | **Evals**: how to know your AI system works | _coming soon_ |

## Setup for participants

1. Open the session notebook with its Colab badge above.
2. In Colab, click the 🔑 **Secrets** icon (left sidebar), add a secret named `ANTHROPIC_API_KEY` with the key from your facilitator, and enable notebook access.
3. Run the cells from the top. The notebook installs Playwright and a headless Chromium (about a minute) and downloads the practice site from this repo.

## Harbor Desk, the practice site

[`harbor_desk.py`](harbor_desk.py) is a small fictional company helpdesk (sign-in, tickets, a dashboard, settings) that runs inside the notebook at `127.0.0.1:8077`. It uses only the Python standard library, keeps everything in memory, and is deterministic, so agents can be tested without touching a real website. Ticket #482 contains a deliberate prompt injection for the security section.

Facilitator helpers (never shown to the agent): `/__state` returns the current data as JSON, `/__reset` restores the seed data. To run it on its own: `python harbor_desk.py`.

*Harbor Desk and everyone in it are fictional.*

<p align="center">
  <img src="https://img.shields.io/badge/ClawHub-downloads-455-blue" alt="ClawHub downloads">
  <img src="https://img.shields.io/badge/python-3.8+-blue" alt="Python 3.8+">
  <img src="https://img.shields.io/badge/license-MIT-yellow" alt="MIT license">
</p>

# 🔍 prompt-inspector

> Scan AI prompts for censorship trigger words before sending — get risk levels, neutral rewrite suggestions, and uncensored system presets.
> Because your AI shouldn't call gardening a satanic act.

---

> *"I literally couldn't get an answer to a gardening question due to supposed 'violence'... Your filter thought my gardening pitchfork was a sign of satanism."* — r/ChatGPT (26↑)

---

## The Problem

You ask an AI a perfectly reasonable question — about gardening, history, or medicine — and it refuses. Your prompt hit a hidden trigger word in the safety filter. You waste time reformulating prompts by trial and error.

## The Solution

One command scans your prompt before you send it. Detects trigger words across 6 categories. Tells you the risk level and suggests neutral rewrites.

```bash
pip install git+https://github.com/minirr890112-byte/prompt-inspector.git
prompt-inspector "write a story about a dictator who uses propaganda"
```

---

## What It Checks

| Category | Risk triggers | Examples |
|----------|--------------|----------|
| Violence | weapons, fighting, combat | "stab", "shoot", "bomb" |
| Self-harm | suicide, cutting, overdose | "kill myself" |
| Adult | explicit content, nudity | flagged terms |
| Politics | regime, censorship, propaganda | "dictator", "oppression" |
| Religion | blasphemy, extremism | flagged terms |
| Drugs | substances, abuse, overdose | flagged terms |

---

## Real Output

```
$ prompt-inspector "write a story about a dictator who uses propaganda"

🔍 prompt-inspector scan results:
────────────────────────────────────────
⚠️  Found 2 potential trigger categories

🔴 Politics (CRITICAL)
   "dictator" — flagged as political violence
   💡 Rewrite: "authoritarian leader", "autocratic figure"

🟡 Politics (MEDIUM)
   "propaganda" — flagged as political manipulation
   💡 Rewrite: "persuasive communication", "state messaging"

📊 Risk score: 45/100
💡 Tip: Replace flagged terms with neutral alternatives above
```

---

## Usage

```bash
# Scan a prompt directly
prompt-inspector "your prompt text here"

# Pipe from stdin
echo "controversial topic" | prompt-inspector

# Scan from file
cat my_prompt.txt | prompt-inspector
```

---

## Features

- **6 trigger categories** — violence, self-harm, adult, politics, religion, drugs
- **Risk levels** — critical / high / medium for each match
- **Rewrite suggestions** — neutral alternatives for every flagged term
- **Stdin support** — pipe prompts from files or other tools
- **Uncensored presets** — ready-to-use system prompts for local models (Gemma, DeepSeek, Llama)

---

## ⭐ Why Star?

ClawHub stats: **455 downloads, 0 stars.**

If an AI has ever refused to answer your perfectly normal question, this tool is for you. Star it so others find it too.

---

## Ecosystem

| Tool | Description |
|------|-------------|
| [code-inspector](https://github.com/minirr890112-byte/code-inspector) | AI code quality scanner |
| [api-cost-compare](https://github.com/minirr890112-byte/api-cost-compare) | Compare LLM API pricing |
| [model-watch](https://github.com/minirr890112-byte/model-watch) | Monitor models for degradation |

Part of [HermesMade](https://github.com/minirr890112-byte/HermesMade) — tools built from real Reddit pain points.

---

<p align="center">
  <b>Scan before you send. Know what triggers the filter.</b><br>
  <sub>MIT License · <a href="https://github.com/minirr890112-byte/prompt-inspector">Give it a star →</a></sub>
</p>

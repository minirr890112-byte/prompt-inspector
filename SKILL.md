---
name: prompt-inspector
description: Scan AI prompts for censorship trigger words across 6 categories (violence, self-harm, adult, politics, religion, drugs). Get neutral rewrite suggestions and uncensored system presets for Gemma/DeepSeek/Llama.
version: 1.2.0
author: minirr890112-byte
license: MIT
metadata:
  hermes:
    tags: [AI, Censorship, Prompt-Engineering, Safety, Content-Filter, Developer-Tools]
    homepage: https://github.com/minirr890112-byte/prompt-inspector
---

# prompt-inspector

## Problem → Solution

**The problem**: You ask an AI a perfectly reasonable question about gardening. The AI flags "pitchfork" as a violent weapon and refuses to answer. Or you're researching propaganda techniques for an academic paper and the model shuts down on "dictator." Censorship is getting stricter, and you don't know which words trigger it until you're blocked.

**The solution**: Scan your prompt before sending it. This tool checks 6 trigger categories and tells you exactly which words will trip the safety filter. It suggests neutral rewrites and academic framing alternatives. Includes uncensored system presets for local models.

## Quick Start

```bash
pip install git+https://github.com/minirr890112-byte/prompt-inspector.git

prompt-inspector "write a story about a dictator who uses propaganda"
echo "your prompt here" | prompt-inspector
cat my_prompt.txt | prompt-inspector
```

## Real Output

```
$ prompt-inspector "write a story about a dictator who uses propaganda"

🔍 prompt-inspector — Censorship Scan
──────────────────────────────────────
⚠️  2 trigger(s) detected

Politics (high risk):
  → "dictator" — may trigger political content filter
  → "propaganda" — may trigger misinformation filter

💡 Suggestions:
  → Replace "dictator" with "authoritarian leader"
  → Replace "propaganda" with "state media narratives"
  → Academic framing: "Analyze 20th century political communication"
```

## 6 Trigger Categories

| Category | Risk Level | Common Triggers |
|----------|-----------|-----------------|
| Violence | Critical | kill, attack, weapon, bomb |
| Self-harm | Critical | suicide, self-harm, cutting |
| Adult | High | explicit terms, NSFW |
| Politics | Medium | dictator, propaganda, regime |
| Religion | Medium | blasphemy, religious violence |
| Drugs | Low | substance names, trafficking |

---
⭐ **Star this repo if an AI ever blocked you for a normal question**: [github.com/minirr890112-byte/prompt-inspector](https://github.com/minirr890112-byte/prompt-inspector)
